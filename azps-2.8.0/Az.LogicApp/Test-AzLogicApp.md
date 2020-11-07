---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/test-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
ms.openlocfilehash: aa1a4148da7958c587363bcfdc11d53ae7a25b7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751471"
---
# <span data-ttu-id="0c79e-101">Test-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="0c79e-101">Test-AzLogicApp</span></span>

## <span data-ttu-id="0c79e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c79e-102">SYNOPSIS</span></span>
<span data-ttu-id="0c79e-103">Mantık uygulaması tanımını doğrular.</span><span class="sxs-lookup"><span data-stu-id="0c79e-103">Validates a logic app definition.</span></span>

## <span data-ttu-id="0c79e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c79e-104">SYNTAX</span></span>

### <span data-ttu-id="0c79e-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c79e-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c79e-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c79e-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c79e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c79e-107">DESCRIPTION</span></span>
<span data-ttu-id="0c79e-108">**Test-Azlogicuyg** cmdlet 'i kaynak grubunda bir mantık uygulaması tanımını doğrular.</span><span class="sxs-lookup"><span data-stu-id="0c79e-108">The **Test-AzLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="0c79e-109">Mantık uygulaması adını, kaynak grubu adını, konumunu, durumu, tümleştirme hesap KIMLIĞINI veya parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="0c79e-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>
<span data-ttu-id="0c79e-110">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="0c79e-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0c79e-111">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="0c79e-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0c79e-112">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="0c79e-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0c79e-113">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="0c79e-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0c79e-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c79e-114">EXAMPLES</span></span>

### <span data-ttu-id="0c79e-115">Örnek 1: dosya yollarını kullanarak bir mantık uygulamasını doğrulama</span><span class="sxs-lookup"><span data-stu-id="0c79e-115">Example 1: Validate a logic app by using file paths</span></span>
```
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="0c79e-116">Bu komut, belirtilen kaynak grubundaki LogicApp01 adındaki bir mantık uygulamasını doğrular.</span><span class="sxs-lookup"><span data-stu-id="0c79e-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="0c79e-117">Komut, tanım ve parametre dosyası yollarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c79e-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="0c79e-118">Örnek 2: nesneleri kullanarak bir mantık uygulamasını doğrulama</span><span class="sxs-lookup"><span data-stu-id="0c79e-118">Example 2: Validate a logic app by using objects</span></span>
```
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="0c79e-119">Bu komut, belirtilen kaynak grubundaki LogicApp01 adındaki bir mantık uygulamasını doğrular.</span><span class="sxs-lookup"><span data-stu-id="0c79e-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="0c79e-120">Komut, tanım ve parametre nesnelerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c79e-120">The command specifies definition and parameter objects.</span></span>

## <span data-ttu-id="0c79e-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c79e-121">PARAMETERS</span></span>

### <span data-ttu-id="0c79e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c79e-122">-DefaultProfile</span></span>
<span data-ttu-id="0c79e-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0c79e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c79e-124">Tanımlı</span><span class="sxs-lookup"><span data-stu-id="0c79e-124">-Definition</span></span>
<span data-ttu-id="0c79e-125">JavaScript nesne gösterimi (JSON) biçiminde bir nesne veya dize olarak bir mantık uygulamasının tanımını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c79e-125">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="0c79e-126">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="0c79e-126">-DefinitionFilePath</span></span>
<span data-ttu-id="0c79e-127">Mantık uygulamanızın tanımını JSON biçimindeki bir tanım dosyasının yolu olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c79e-127">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="0c79e-128">-Integrationaccountıd</span><span class="sxs-lookup"><span data-stu-id="0c79e-128">-IntegrationAccountId</span></span>
<span data-ttu-id="0c79e-129">Mantık uygulaması için bir tümleştirme hesap KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c79e-129">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="0c79e-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="0c79e-130">-Location</span></span>
<span data-ttu-id="0c79e-131">Mantık uygulamasının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c79e-131">Specifies the location of the logic app.</span></span>
<span data-ttu-id="0c79e-132">Batı ABD veya Güneydoğu Asya gibi bir Azure veri merkezi konumu girin.</span><span class="sxs-lookup"><span data-stu-id="0c79e-132">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="0c79e-133">Herhangi bir konuma bir mantık uygulaması yerleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0c79e-133">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="0c79e-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="0c79e-134">-Name</span></span>
<span data-ttu-id="0c79e-135">Mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c79e-135">Specifies the name of the logic app.</span></span>

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

### <span data-ttu-id="0c79e-136">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="0c79e-136">-ParameterFilePath</span></span>
<span data-ttu-id="0c79e-137">JSON biçimli parametre dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c79e-137">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="0c79e-138">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="0c79e-138">-Parameters</span></span>
<span data-ttu-id="0c79e-139">Mantık uygulamasının parametre koleksiyonu nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c79e-139">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="0c79e-140">Karma tablo, sözlük \< dizesi \> veya sözlük \< dizesi, WorkflowParameter belirtin \> .</span><span class="sxs-lookup"><span data-stu-id="0c79e-140">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="0c79e-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c79e-141">-ResourceGroupName</span></span>
<span data-ttu-id="0c79e-142">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c79e-142">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0c79e-143">Durumlu</span><span class="sxs-lookup"><span data-stu-id="0c79e-143">-State</span></span>
<span data-ttu-id="0c79e-144">Mantık uygulamasının durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c79e-144">Specifies a state of the logic app.</span></span>
<span data-ttu-id="0c79e-145">Bu parametre için kabul edilebilir değerler: etkin ve devre dışı.</span><span class="sxs-lookup"><span data-stu-id="0c79e-145">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="0c79e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c79e-146">CommonParameters</span></span>
<span data-ttu-id="0c79e-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c79e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c79e-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c79e-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c79e-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c79e-149">INPUTS</span></span>

### <span data-ttu-id="0c79e-150">System. String</span><span class="sxs-lookup"><span data-stu-id="0c79e-150">System.String</span></span>

## <span data-ttu-id="0c79e-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c79e-151">OUTPUTS</span></span>

### <span data-ttu-id="0c79e-152">System. void</span><span class="sxs-lookup"><span data-stu-id="0c79e-152">System.Void</span></span>

## <span data-ttu-id="0c79e-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c79e-153">NOTES</span></span>

## <span data-ttu-id="0c79e-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c79e-154">RELATED LINKS</span></span>

[<span data-ttu-id="0c79e-155">Get-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="0c79e-155">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="0c79e-156">Yeni-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="0c79e-156">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="0c79e-157">Remove-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="0c79e-157">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="0c79e-158">Set-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="0c79e-158">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="0c79e-159">Start-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="0c79e-159">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


