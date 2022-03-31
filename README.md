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
        nombres.Add("Changbin");
        nombres.Add("Bangchan");
        nombres.Add("Jungkook");
        nombres.Add("Suga");
        nombres.Add("Felix");
        if(texto == null){
            Debug.Log("testo sin asignar");
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
