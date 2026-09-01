# sitedorafaelusing UnityEngine;

public class Arma : MonoBehaviour
{
    [Header("Configurações do Disparo")]
    public Transform pontoDeDisparo; // Ponto de onde a bala/raio sai
    public float alcance = 100f;
    public float dano = 25f;
    public float cadenciaDeTiro = 0.15f;

    [Header("Efeitos")]
    public ParticleSystem efeitoMuzzle;
    public GameObject impactoPrefabusing UnityEngine;

public class Arma : MonoBehaviour
{
    [Header("Configurações do Disparo")]
    public Transform pontoDeDisparo; // Ponto de onde a bala/raio sai
    public float alcance = 100f;
    public float dano = 25f;
    public float cadenciaDeTiro = 0.15f;

    [Header("Efeitos")]
    public ParticleSystem efeitoMuzzle;
    public GameObject impactoPrefab;

    private float proximoTiro = 0f;

    void Update()
    {
        // Dispara quando pressiona o botão esquerdo do mouse
        if (Input.GetButton("Fire1"using UnityEngine;

public class Arma : MonoBehaviour
{
    [Header("Configurações do Disparo")]
    public Transform pontoDeDisparo; // Ponto de onde a bala/raio sai
    public float alcance = 100f;
    public float dano = 25f;
    public float cadenciaDeTiro = 0.15f;

    [Header("Efeitos")]
    public ParticleSystem efeitoMuzzle;
    public GameObject impactoPrefab;

    private float proximoTiro = 0f;

    void Update()
    {
        // Dispara quando pressiona o botão esquerdo do mouse
        if (Input.GetButton("Fire1") && Time.time >= proximoTiro)
        {
            proximoTiro = Time.time + cadenciaDeTiro;
            Atirar();
        }
    }

    void Atirar()
    {
        if (efeitoMuzzle != null)
            efeitoMuzzle.Play();

        RaycastHit hit;
        // Não há consumo de munição aqui, permitindo disparos infinitos
        if (Physics.Raycast(pontoDeDisparo.position, pontoDeDisparo.forward, out hit, alcance))
        {
            Debug.Log("Atingiu: " + hit.transform.name);

            // Instancia efeito de impacto no ponto atingido
            if (impactoPrefab != null)
            {
                Instantiate(impactoPrefab, hit.point, Quaternion.LookRotation(hit.normal));
            }
        }
    }
}) && Time.time >= proximoTiro)
        {
            proximoTiro = Time.time + cadenciaDeTiro;
            Atirar();
        }
    }

    void Atirar()
    {
        if (efeitoMuzzle != null)
            efeitoMuzzle.Play();

        RaycastHit hit;
        // Não há consumo de munição aqui, permitindo disparos infinitos
        if (Physics.Raycast(pontoDeDisparo.position, pontoDeDisparo.forward, out hit, alcance))
        {
            Debug.Log("Atingiu: " + hit.transform.name);

            // Instancia efeito de impacto no ponto atingido
            if (impactoPrefab != null)
            {
                Instantiate(impactoPrefab, hit.point, Quaternion.LookRotation(hit.normal));
            }
        }
    }
};

    private float proximoTiro = 0f;

    void Update()
    {
        // Dispara quando pressiona o botão esquerdo do mouse
        if (Input.GetButton("Fire1") && Time.time >= proximoTiro)
        {
            proximoTiro = Time.time + cadenciaDeTiro;
            Atirar();
        }
    }

    void Atirar()
    {
        if (efeitoMuzzle != null)
            efeitoMuzzle.Play();

        RaycastHit hit;
        // Não há consumo de muniçusing UnityEngine;

public class Arma : MonoBehaviour
{
    [Header("Configurações do Disparo")]
    public Transform pontoDeDisparo; // Ponto de onde a bala/raio sai
    public float alcance = 100f;
    public float dano = 25f;
    public float cadenciaDeTiro = 0.15f;

    [Header("Efeitos")]
    public ParticleSystem efeitoMuzzle;
    public GameObject impactoPrefab;

    private float proximoTiro = 0f;

    void Update()
    {
        // Dispara quando pressiona o botão esquerdo do mouse
        if (Input.GetButton("Fire1") && Time.time >= proximoTiro)
        {
            proximoTiro = Time.time + cadenciaDeTiro;
            Atirar();
        }
    }

    void Atirar()
    {
        if (efeitoMuzzle != null)
            efeitoMuzzle.Play();

        RaycastHit hit;
        // Não há consumo de munição aqui, permitindo disparos infinitos
        if (Physics.Raycast(pontoDeDisparo.position, pontoDeDisparo.forward, out hit, alcance))
        {
            Debug.Log("Atingiu: " + hit.transform.name);

            // Instancia efeito de impacto no ponto atingido
            if (impactoPrefab != null)
            {
                Instantiate(impactoPrefab, hit.point, Quaternion.LookRotation(hit.normal));
            }
        }
    }
}ão aqui, permitindo disparos infinitos
        if (Physics.Raycast(pontoDeDisparo.position, pontoDeDisparo.forward, out hit, alcance))
        {
            Debug.Log("Atingiu: " + hit.transform.name);

            // Instancia efeito de impacto no ponto atingido
            if (impactoPrefab != null)
            {
                Instantiate(impactoPrefab, hit.point, Quaternion.LookRotation(hit.normal));
            }
        }
    }
}