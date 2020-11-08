---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/test-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
ms.openlocfilehash: d38363d27253bea023e837e9b84076ccdcbf2b8d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278943"
---
# <span data-ttu-id="18f1e-101">Test-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="18f1e-101">Test-AzLogicApp</span></span>

## <span data-ttu-id="18f1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18f1e-102">SYNOPSIS</span></span>
<span data-ttu-id="18f1e-103">Mantık uygulaması tanımını doğrular.</span><span class="sxs-lookup"><span data-stu-id="18f1e-103">Validates a logic app definition.</span></span>

## <span data-ttu-id="18f1e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="18f1e-104">SYNTAX</span></span>

### <span data-ttu-id="18f1e-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="18f1e-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18f1e-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="18f1e-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18f1e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="18f1e-107">DESCRIPTION</span></span>
<span data-ttu-id="18f1e-108">**Test-Azlogicuyg** cmdlet 'i kaynak grubunda bir mantık uygulaması tanımını doğrular.</span><span class="sxs-lookup"><span data-stu-id="18f1e-108">The **Test-AzLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="18f1e-109">Mantık uygulaması adını, kaynak grubu adını, konumunu, durumu, tümleştirme hesap KIMLIĞINI veya parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="18f1e-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>
<span data-ttu-id="18f1e-110">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="18f1e-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="18f1e-111">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="18f1e-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="18f1e-112">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="18f1e-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="18f1e-113">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="18f1e-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="18f1e-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="18f1e-114">EXAMPLES</span></span>

### <span data-ttu-id="18f1e-115">Örnek 1: dosya yollarını kullanarak bir mantık uygulamasını doğrulama</span><span class="sxs-lookup"><span data-stu-id="18f1e-115">Example 1: Validate a logic app by using file paths</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="18f1e-116">Bu komut, belirtilen kaynak grubundaki LogicApp01 adındaki bir mantık uygulamasını doğrular.</span><span class="sxs-lookup"><span data-stu-id="18f1e-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="18f1e-117">Komut, tanım ve parametre dosyası yollarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18f1e-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="18f1e-118">Örnek 2: nesneleri kullanarak bir mantık uygulamasını doğrulama</span><span class="sxs-lookup"><span data-stu-id="18f1e-118">Example 2: Validate a logic app by using objects</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="18f1e-119">Bu komut, belirtilen kaynak grubundaki LogicApp01 adındaki bir mantık uygulamasını doğrular.</span><span class="sxs-lookup"><span data-stu-id="18f1e-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="18f1e-120">Komut, tanım ve parametre nesnelerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="18f1e-120">The command specifies definition and parameter objects.</span></span>

### <span data-ttu-id="18f1e-121">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="18f1e-121">Example 3</span></span>

<span data-ttu-id="18f1e-122">Mantık uygulaması tanımını doğrular.</span><span class="sxs-lookup"><span data-stu-id="18f1e-122">Validates a logic app definition.</span></span> <span data-ttu-id="18f1e-123">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="18f1e-123">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Test-AzLogicApp -DefinitionFilePath 'd:\workflows\Definition.json' -IntegrationAccountId <String> -Location 'westus' -Name 'LogicApp01' -ParameterFilePath 'd:\workflows\Parameters.json' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="18f1e-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="18f1e-124">PARAMETERS</span></span>

### <span data-ttu-id="18f1e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18f1e-125">-DefaultProfile</span></span>
<span data-ttu-id="18f1e-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="18f1e-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f1e-127">Tanımlı</span><span class="sxs-lookup"><span data-stu-id="18f1e-127">-Definition</span></span>
<span data-ttu-id="18f1e-128">JavaScript nesne gösterimi (JSON) biçiminde bir nesne veya dize olarak bir mantık uygulamasının tanımını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18f1e-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="18f1e-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="18f1e-129">-DefinitionFilePath</span></span>
<span data-ttu-id="18f1e-130">Mantık uygulamanızın tanımını JSON biçimindeki bir tanım dosyasının yolu olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="18f1e-130">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="18f1e-131">-Integrationaccountıd</span><span class="sxs-lookup"><span data-stu-id="18f1e-131">-IntegrationAccountId</span></span>
<span data-ttu-id="18f1e-132">Mantık uygulaması için bir tümleştirme hesap KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="18f1e-132">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="18f1e-133">-Konum</span><span class="sxs-lookup"><span data-stu-id="18f1e-133">-Location</span></span>
<span data-ttu-id="18f1e-134">Mantık uygulamasının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="18f1e-134">Specifies the location of the logic app.</span></span>
<span data-ttu-id="18f1e-135">Batı ABD veya Güneydoğu Asya gibi bir Azure veri merkezi konumu girin.</span><span class="sxs-lookup"><span data-stu-id="18f1e-135">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="18f1e-136">Herhangi bir konuma bir mantık uygulaması yerleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="18f1e-136">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="18f1e-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="18f1e-137">-Name</span></span>
<span data-ttu-id="18f1e-138">Mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18f1e-138">Specifies the name of the logic app.</span></span>

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

### <span data-ttu-id="18f1e-139">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="18f1e-139">-ParameterFilePath</span></span>
<span data-ttu-id="18f1e-140">JSON biçimli parametre dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="18f1e-140">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="18f1e-141">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="18f1e-141">-Parameters</span></span>
<span data-ttu-id="18f1e-142">Mantık uygulamasının parametre koleksiyonu nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="18f1e-142">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="18f1e-143">Karma tablo, sözlük \<string\> veya sözlük belirtin \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="18f1e-143">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="18f1e-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18f1e-144">-ResourceGroupName</span></span>
<span data-ttu-id="18f1e-145">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18f1e-145">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="18f1e-146">Durumlu</span><span class="sxs-lookup"><span data-stu-id="18f1e-146">-State</span></span>
<span data-ttu-id="18f1e-147">Mantık uygulamasının durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="18f1e-147">Specifies a state of the logic app.</span></span>
<span data-ttu-id="18f1e-148">Bu parametre için kabul edilebilir değerler: etkin ve devre dışı.</span><span class="sxs-lookup"><span data-stu-id="18f1e-148">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="18f1e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18f1e-149">CommonParameters</span></span>
<span data-ttu-id="18f1e-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="18f1e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18f1e-151">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18f1e-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18f1e-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="18f1e-152">INPUTS</span></span>

### <span data-ttu-id="18f1e-153">System. String</span><span class="sxs-lookup"><span data-stu-id="18f1e-153">System.String</span></span>

## <span data-ttu-id="18f1e-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="18f1e-154">OUTPUTS</span></span>

### <span data-ttu-id="18f1e-155">System. void</span><span class="sxs-lookup"><span data-stu-id="18f1e-155">System.Void</span></span>

## <span data-ttu-id="18f1e-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="18f1e-156">NOTES</span></span>

## <span data-ttu-id="18f1e-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="18f1e-157">RELATED LINKS</span></span>

[<span data-ttu-id="18f1e-158">Get-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="18f1e-158">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="18f1e-159">Yeni-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="18f1e-159">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="18f1e-160">Remove-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="18f1e-160">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="18f1e-161">Set-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="18f1e-161">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="18f1e-162">Start-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="18f1e-162">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


