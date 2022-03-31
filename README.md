# AleatorioText

using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using TMPro;

public class TextController : MonoBehaviour
{
    public static TextController instance;
    public TextMeshProUGUI texto;
    public List<string> nombres = new List<string>();

    void Awake() {
        instance = this;
    }
    // Start is called before the first frame update
    void Start()
    {
        nombres.Add("Julio");
        nombres.Add("Fran");
        nombres.Add("Pepe");
        nombres.Add("Manolo");
        nombres.Add("Paco");
        if(texto == null){
            Debug.Log("texto no asignado");
        }
        else {
            texto.text = nombres[Random.Range(0, nombres.Count)].ToString();
        }
    }

    // Update is called once per frame
    void Update()
    {
        
    }
}
