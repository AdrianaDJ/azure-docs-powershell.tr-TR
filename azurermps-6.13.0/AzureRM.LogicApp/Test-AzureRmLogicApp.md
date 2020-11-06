---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/test-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Test-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Test-AzureRmLogicApp.md
ms.openlocfilehash: 35ce8352670aa2af2a7051736e1b986b83bcc64b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590898"
---
# <span data-ttu-id="d4997-101">Test-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="d4997-101">Test-AzureRmLogicApp</span></span>

## <span data-ttu-id="d4997-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4997-102">SYNOPSIS</span></span>
<span data-ttu-id="d4997-103">Mantık uygulaması tanımını doğrular.</span><span class="sxs-lookup"><span data-stu-id="d4997-103">Validates a logic app definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4997-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d4997-104">SYNTAX</span></span>

### <span data-ttu-id="d4997-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4997-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4997-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4997-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4997-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d4997-107">DESCRIPTION</span></span>
<span data-ttu-id="d4997-108">**Test-Azurermlogicuyg** cmdlet 'i kaynak grubunda bir mantık uygulaması tanımını doğrular.</span><span class="sxs-lookup"><span data-stu-id="d4997-108">The **Test-AzureRmLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="d4997-109">Mantık uygulaması adını, kaynak grubu adını, konumunu, durumu, tümleştirme hesap KIMLIĞINI veya parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="d4997-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>
<span data-ttu-id="d4997-110">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="d4997-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d4997-111">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="d4997-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d4997-112">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="d4997-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d4997-113">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="d4997-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d4997-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d4997-114">EXAMPLES</span></span>

### <span data-ttu-id="d4997-115">Örnek 1: dosya yollarını kullanarak bir mantık uygulamasını doğrulama</span><span class="sxs-lookup"><span data-stu-id="d4997-115">Example 1: Validate a logic app by using file paths</span></span>
```
PS C:\>Test-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="d4997-116">Bu komut, belirtilen kaynak grubundaki LogicApp01 adındaki bir mantık uygulamasını doğrular.</span><span class="sxs-lookup"><span data-stu-id="d4997-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="d4997-117">Komut, tanım ve parametre dosyası yollarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4997-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="d4997-118">Örnek 2: nesneleri kullanarak bir mantık uygulamasını doğrulama</span><span class="sxs-lookup"><span data-stu-id="d4997-118">Example 2: Validate a logic app by using objects</span></span>
```
PS C:\>Test-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="d4997-119">Bu komut, belirtilen kaynak grubundaki LogicApp01 adındaki bir mantık uygulamasını doğrular.</span><span class="sxs-lookup"><span data-stu-id="d4997-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="d4997-120">Komut, tanım ve parametre nesnelerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4997-120">The command specifies definition and parameter objects.</span></span>

## <span data-ttu-id="d4997-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d4997-121">PARAMETERS</span></span>

### <span data-ttu-id="d4997-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4997-122">-DefaultProfile</span></span>
<span data-ttu-id="d4997-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d4997-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4997-124">Tanımlı</span><span class="sxs-lookup"><span data-stu-id="d4997-124">-Definition</span></span>
<span data-ttu-id="d4997-125">JavaScript nesne gösterimi (JSON) biçiminde bir nesne veya dize olarak bir mantık uygulamasının tanımını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4997-125">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: System.Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4997-126">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="d4997-126">-DefinitionFilePath</span></span>
<span data-ttu-id="d4997-127">Mantık uygulamanızın tanımını JSON biçimindeki bir tanım dosyasının yolu olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4997-127">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4997-128">-Integrationaccountıd</span><span class="sxs-lookup"><span data-stu-id="d4997-128">-IntegrationAccountId</span></span>
<span data-ttu-id="d4997-129">Mantık uygulaması için bir tümleştirme hesap KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4997-129">Specifies an integration account ID for the logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4997-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="d4997-130">-Location</span></span>
<span data-ttu-id="d4997-131">Mantık uygulamasının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4997-131">Specifies the location of the logic app.</span></span>
<span data-ttu-id="d4997-132">Batı ABD veya Güneydoğu Asya gibi bir Azure veri merkezi konumu girin.</span><span class="sxs-lookup"><span data-stu-id="d4997-132">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="d4997-133">Herhangi bir konuma bir mantık uygulaması yerleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d4997-133">You can place a logic app in any location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4997-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="d4997-134">-Name</span></span>
<span data-ttu-id="d4997-135">Mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4997-135">Specifies the name of the logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4997-136">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="d4997-136">-ParameterFilePath</span></span>
<span data-ttu-id="d4997-137">JSON biçimli parametre dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4997-137">Specifies the path of a JSON formatted parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4997-138">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="d4997-138">-Parameters</span></span>
<span data-ttu-id="d4997-139">Mantık uygulamasının parametre koleksiyonu nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4997-139">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="d4997-140">Karma tablo, sözlük \<string\> veya sözlük belirtin \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="d4997-140">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4997-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4997-141">-ResourceGroupName</span></span>
<span data-ttu-id="d4997-142">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4997-142">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4997-143">Durumlu</span><span class="sxs-lookup"><span data-stu-id="d4997-143">-State</span></span>
<span data-ttu-id="d4997-144">Mantık uygulamasının durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4997-144">Specifies a state of the logic app.</span></span>
<span data-ttu-id="d4997-145">Bu parametre için kabul edilebilir değerler: etkin ve devre dışı.</span><span class="sxs-lookup"><span data-stu-id="d4997-145">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4997-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4997-146">CommonParameters</span></span>
<span data-ttu-id="d4997-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d4997-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4997-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4997-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4997-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d4997-149">INPUTS</span></span>

### <span data-ttu-id="d4997-150">System. String</span><span class="sxs-lookup"><span data-stu-id="d4997-150">System.String</span></span>

## <span data-ttu-id="d4997-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d4997-151">OUTPUTS</span></span>

### <span data-ttu-id="d4997-152">System. void</span><span class="sxs-lookup"><span data-stu-id="d4997-152">System.Void</span></span>

## <span data-ttu-id="d4997-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d4997-153">NOTES</span></span>

## <span data-ttu-id="d4997-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d4997-154">RELATED LINKS</span></span>

[<span data-ttu-id="d4997-155">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="d4997-155">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="d4997-156">Yeni-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="d4997-156">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="d4997-157">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="d4997-157">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="d4997-158">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="d4997-158">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="d4997-159">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="d4997-159">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


