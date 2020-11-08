---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 34f09ca41326b2f6686a41cdeba0910317bc7a2c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279234"
---
# <span data-ttu-id="f423e-101">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="f423e-101">Start-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="f423e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f423e-102">SYNOPSIS</span></span>
<span data-ttu-id="f423e-103">Otomasyon 'da bir DSC yapılandırmasını derler.</span><span class="sxs-lookup"><span data-stu-id="f423e-103">Compiles a DSC configuration in Automation.</span></span>

## <span data-ttu-id="f423e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f423e-104">SYNTAX</span></span>

```
Start-AzAutomationDscCompilationJob [-ConfigurationName] <String> [-Parameters <IDictionary>]
 [-ConfigurationData <IDictionary>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f423e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f423e-105">DESCRIPTION</span></span>
<span data-ttu-id="f423e-106">**Start-AzAutomationDscCompilationJob** cmdlet 'ı, Azure Otomasyonu 'Nda APS Istenen durum yapılandırma (DSC) yapılandırmasını derler.</span><span class="sxs-lookup"><span data-stu-id="f423e-106">The **Start-AzAutomationDscCompilationJob** cmdlet compiles an APS Desired State Configuration (DSC) configuration in Azure Automation.</span></span>

## <span data-ttu-id="f423e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f423e-107">EXAMPLES</span></span>

### <span data-ttu-id="f423e-108">Örnek 1: Otomasyonda Azure DSC yapılandırmasını derleme</span><span class="sxs-lookup"><span data-stu-id="f423e-108">Example 1: Compile an Azure DSC configuration in Automation</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f423e-109">İlk komut, bir parametre sözlüğü oluşturur ve bunları $Params değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f423e-109">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="f423e-110">İkinci komut, Config01 adlı DSC yapılandırmasını derler.</span><span class="sxs-lookup"><span data-stu-id="f423e-110">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="f423e-111">Komut, DSC yapılandırma parametreleri için $Params değerleri içerir.</span><span class="sxs-lookup"><span data-stu-id="f423e-111">The command includes the values in $Params for DSC configuration parameters.</span></span>

### <span data-ttu-id="f423e-112">Örnek 2: yeni bir düğüm yapılandırması derleme sürümüyle bir Azure DSC yapılandırmasını Otomasyon 'da derleyin.</span><span class="sxs-lookup"><span data-stu-id="f423e-112">Example 2: Compile an Azure DSC configuration in Automation with a new Node Configuration build version.</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="f423e-113">İlk örnekle benzer şekilde, ilk komut bir parametre sözlüğü oluşturur ve bunları $Params değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f423e-113">Similar to the first example, the first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="f423e-114">İkinci komut, Config01 adlı DSC yapılandırmasını derler.</span><span class="sxs-lookup"><span data-stu-id="f423e-114">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="f423e-115">Komut, DSC yapılandırma parametreleri için $Params değerleri içerir.</span><span class="sxs-lookup"><span data-stu-id="f423e-115">The command includes the values in $Params for DSC configuration parameters.</span></span>
<span data-ttu-id="f423e-116">Config01 [<2>] adıyla yeni bir düğüm yapılandırması oluşturarak önceki mevcut düğüm yapılandırmasını geçersiz kılmaz <NodeName> .</span><span class="sxs-lookup"><span data-stu-id="f423e-116">It does not override the earlier existing Node Configuration by creating a new Node Configuration with the name Config01[<2>].<NodeName>.</span></span> <span data-ttu-id="f423e-117">Sürüm numarası zaten mevcut olan sürüm numarası temel alınarak artırılır.</span><span class="sxs-lookup"><span data-stu-id="f423e-117">The version number is incremented based on the existing version number already present.</span></span>

## <span data-ttu-id="f423e-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f423e-118">PARAMETERS</span></span>

### <span data-ttu-id="f423e-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f423e-119">-AutomationAccountName</span></span>
<span data-ttu-id="f423e-120">Bu cmdlet 'in derolduğu DSC yapılandırmasını içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f423e-120">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f423e-121">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="f423e-121">-ConfigurationData</span></span>
<span data-ttu-id="f423e-122">DSC yapılandırması için yapılandırma verilerinin sözlüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f423e-122">Specifies a dictionary of configuration data for DSC configuration.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f423e-123">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f423e-123">-ConfigurationName</span></span>
<span data-ttu-id="f423e-124">Bu cmdlet 'in derolduğu DSC yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f423e-124">Specifies the name of the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f423e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f423e-125">-DefaultProfile</span></span>
<span data-ttu-id="f423e-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f423e-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f423e-127">-Incrementnodeconfigurationbuıld</span><span class="sxs-lookup"><span data-stu-id="f423e-127">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="f423e-128">Yeni bir düğüm yapılandırması derleme sürümü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f423e-128">Creates a new Node Configuration build version.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f423e-129">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="f423e-129">-Parameters</span></span>
<span data-ttu-id="f423e-130">Bu cmdlet 'in DSC yapılandırmasını derlemek için kullandığı parametrelerin sözlüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f423e-130">Specifies a dictionary of parameters that this cmdlet uses to compile the DSC configuration.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f423e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f423e-131">-ResourceGroupName</span></span>
<span data-ttu-id="f423e-132">Bu cmdlet 'in bir yapılandırmayı derlediğini belirten bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f423e-132">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f423e-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="f423e-133">-Confirm</span></span>
<span data-ttu-id="f423e-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f423e-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f423e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f423e-135">-WhatIf</span></span>
<span data-ttu-id="f423e-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f423e-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f423e-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f423e-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f423e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f423e-138">CommonParameters</span></span>
<span data-ttu-id="f423e-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f423e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f423e-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f423e-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f423e-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f423e-141">INPUTS</span></span>

### <span data-ttu-id="f423e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f423e-142">System.String</span></span>

## <span data-ttu-id="f423e-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f423e-143">OUTPUTS</span></span>

### <span data-ttu-id="f423e-144">Microsoft. Azure. Commands. Automation. model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="f423e-144">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="f423e-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f423e-145">NOTES</span></span>

## <span data-ttu-id="f423e-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f423e-146">RELATED LINKS</span></span>

[<span data-ttu-id="f423e-147">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="f423e-147">Get-AzAutomationDscCompilationJob</span></span>](./Get-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="f423e-148">Get-Azautomationdsccompilationjoi Input</span><span class="sxs-lookup"><span data-stu-id="f423e-148">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)


