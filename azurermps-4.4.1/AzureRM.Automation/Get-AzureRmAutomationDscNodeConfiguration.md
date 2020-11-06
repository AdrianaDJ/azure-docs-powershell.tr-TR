---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: f5de98b4f64b4f9adb03493638cdf4e1e613e10f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591203"
---
# <span data-ttu-id="f6959-101">Get-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6959-101">Get-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="f6959-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6959-102">SYNOPSIS</span></span>
<span data-ttu-id="f6959-103">Otomasyon 'daki DSC düğüm yapılandırmalarının meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="f6959-103">Gets metadata for DSC node configurations in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6959-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f6959-104">SYNTAX</span></span>

### <span data-ttu-id="f6959-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f6959-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6959-106">ByNodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f6959-106">ByNodeConfigurationName</span></span>
```
Get-AzureRmAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6959-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f6959-107">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6959-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f6959-108">DESCRIPTION</span></span>
<span data-ttu-id="f6959-109">**Get-AzureRmAutomationDscNodeConfiguration** cmdlet 'i, tüm APS</span><span class="sxs-lookup"><span data-stu-id="f6959-109">The **Get-AzureRmAutomationDscNodeConfiguration** cmdlet gets metadata for APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="f6959-110">Automation, DSC düğüm yapılandırmasını yönetilen nesne biçimi (MOF) yapılandırma belgesi olarak depolar.</span><span class="sxs-lookup"><span data-stu-id="f6959-110">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="f6959-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f6959-111">EXAMPLES</span></span>

### <span data-ttu-id="f6959-112">Örnek 1: tüm DSC düğüm yapılandırmalarını alma</span><span class="sxs-lookup"><span data-stu-id="f6959-112">Example 1: Get all DSC node configurations</span></span>
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="f6959-113">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm DSC düğüm yapılandırmalarının meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="f6959-113">This command gets metadata for all DSC node configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f6959-114">Örnek 2: DSC yapılandırması için tüm DSC düğüm yapılandırmalarını alma</span><span class="sxs-lookup"><span data-stu-id="f6959-114">Example 2: Get all DSC node configurations for a DSC configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="f6959-115">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm DSC düğüm yapılandırmalarının meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="f6959-115">This command gets metadata for all DSC node configurations in the Automation account named Contoso17 that the DSC configuration named ContosoConfiguration generated.</span></span>

### <span data-ttu-id="f6959-116">Örnek 3: ada göre bir DSC düğüm yapılandırması alma</span><span class="sxs-lookup"><span data-stu-id="f6959-116">Example 3: Get a DSC node configuration by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

<span data-ttu-id="f6959-117">Bu komut, Contoso17 adlı Otomasyon hesabında ContosoConfiguration. webserver adıyla bir DSC düğüm yapılandırmasının meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="f6959-117">This command gets metadata for a DSC node configuration with the name ContosoConfiguration.webserver in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="f6959-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f6959-118">PARAMETERS</span></span>

### <span data-ttu-id="f6959-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f6959-119">-AutomationAccountName</span></span>
<span data-ttu-id="f6959-120">Bu cmdlet 'in meta veri aldığı DSC düğüm yapılandırmalarını içeren bir Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6959-120">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="f6959-121">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f6959-121">-ConfigurationName</span></span>
<span data-ttu-id="f6959-122">Bu cmdlet 'in düğüm yapılandırma meta verilerini aldığı DSC yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6959-122">Specifies the name of DSC configuration for which this cmdlet gets node configuration metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6959-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="f6959-123">-Name</span></span>
<span data-ttu-id="f6959-124">Bu cmdlet 'in meta veri aldığı DSC düğüm yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6959-124">Specifies the name of the DSC node configuration for which this cmdlet gets metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeConfigurationName
Aliases: NodeConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6959-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6959-125">-ResourceGroupName</span></span>
<span data-ttu-id="f6959-126">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6959-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="f6959-127">Bu cmdlet, bu parametrenin belirttiği kaynak grubundaki DSC düğüm yapılandırmalarının meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="f6959-127">This cmdlet gets metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f6959-128">-RollupStatus</span><span class="sxs-lookup"><span data-stu-id="f6959-128">-RollupStatus</span></span>
<span data-ttu-id="f6959-129">Bu cmdlet 'in aldığı DSC düğüm yapılandırmalarının toplama durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6959-129">Specifies the rollup status of DSC node configurations that this cmdlet gets.</span></span>
<span data-ttu-id="f6959-130">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="f6959-130">Valid values are:</span></span> 

- <span data-ttu-id="f6959-131">Kötü</span><span class="sxs-lookup"><span data-stu-id="f6959-131">Bad</span></span> 
- <span data-ttu-id="f6959-132">Gerçekleştireceğiniz</span><span class="sxs-lookup"><span data-stu-id="f6959-132">Good</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases: 
Accepted values: Good, Bad

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6959-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6959-133">-DefaultProfile</span></span>
<span data-ttu-id="f6959-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f6959-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6959-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6959-135">CommonParameters</span></span>
<span data-ttu-id="f6959-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f6959-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6959-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6959-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6959-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f6959-138">INPUTS</span></span>

## <span data-ttu-id="f6959-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f6959-139">OUTPUTS</span></span>

### <span data-ttu-id="f6959-140">Microsoft. Azure. Commands. Automation. model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="f6959-140">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="f6959-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f6959-141">NOTES</span></span>

## <span data-ttu-id="f6959-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f6959-142">RELATED LINKS</span></span>

[<span data-ttu-id="f6959-143">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6959-143">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)


