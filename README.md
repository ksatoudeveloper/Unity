        TextGenerator textGenerator = new TextGenerator();
        Vector2 sizeDelta = text.GetComponent<RectTransform>().sizeDelta;
        textGenerator.Populate(text.text, text.GetGenerationSettings(sizeDelta));
        for (int i = 0; i < text.text.Length; i++)
        {
            Debug.Log("LeftTop:" + textGenerator.verts[i * 4].position);
            Debug.Log("RightBottom:" + textGenerator.verts[i * 4 + 2].position);
        }
