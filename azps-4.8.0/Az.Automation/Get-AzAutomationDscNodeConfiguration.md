---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 1114d0a78518c33126f28fb4b409a881a52a4ae7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273725"
---
# <span data-ttu-id="3638d-101">Get-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="3638d-101">Get-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="3638d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3638d-102">SYNOPSIS</span></span>
<span data-ttu-id="3638d-103">Otomasyon 'daki DSC düğüm yapılandırmalarının meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="3638d-103">Gets metadata for DSC node configurations in Automation.</span></span>

## <span data-ttu-id="3638d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3638d-104">SYNTAX</span></span>

### <span data-ttu-id="3638d-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3638d-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3638d-106">ByNodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="3638d-106">ByNodeConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3638d-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="3638d-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3638d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3638d-108">DESCRIPTION</span></span>
<span data-ttu-id="3638d-109">**Get-AzAutomationDscNodeConfiguration** cmdlet 'i, tüm APS</span><span class="sxs-lookup"><span data-stu-id="3638d-109">The **Get-AzAutomationDscNodeConfiguration** cmdlet gets metadata for APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="3638d-110">Automation, DSC düğüm yapılandırmasını yönetilen nesne biçimi (MOF) yapılandırma belgesi olarak depolar.</span><span class="sxs-lookup"><span data-stu-id="3638d-110">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="3638d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3638d-111">EXAMPLES</span></span>

### <span data-ttu-id="3638d-112">Örnek 1: tüm DSC düğüm yapılandırmalarını alma</span><span class="sxs-lookup"><span data-stu-id="3638d-112">Example 1: Get all DSC node configurations</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="3638d-113">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm DSC düğüm yapılandırmalarının meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="3638d-113">This command gets metadata for all DSC node configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="3638d-114">Örnek 2: DSC yapılandırması için tüm DSC düğüm yapılandırmalarını alma</span><span class="sxs-lookup"><span data-stu-id="3638d-114">Example 2: Get all DSC node configurations for a DSC configuration</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="3638d-115">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm DSC düğüm yapılandırmalarının meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="3638d-115">This command gets metadata for all DSC node configurations in the Automation account named Contoso17 that the DSC configuration named ContosoConfiguration generated.</span></span>

### <span data-ttu-id="3638d-116">Örnek 3: ada göre bir DSC düğüm yapılandırması alma</span><span class="sxs-lookup"><span data-stu-id="3638d-116">Example 3: Get a DSC node configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

<span data-ttu-id="3638d-117">Bu komut, Contoso17 adlı Otomasyon hesabında ContosoConfiguration. webserver adıyla bir DSC düğüm yapılandırmasının meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="3638d-117">This command gets metadata for a DSC node configuration with the name ContosoConfiguration.webserver in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="3638d-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3638d-118">PARAMETERS</span></span>

### <span data-ttu-id="3638d-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3638d-119">-AutomationAccountName</span></span>
<span data-ttu-id="3638d-120">Bu cmdlet 'in meta veri aldığı DSC düğüm yapılandırmalarını içeren bir Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3638d-120">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="3638d-121">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="3638d-121">-ConfigurationName</span></span>
<span data-ttu-id="3638d-122">Bu cmdlet 'in düğüm yapılandırma meta verilerini aldığı DSC yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3638d-122">Specifies the name of DSC configuration for which this cmdlet gets node configuration metadata.</span></span>

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

### <span data-ttu-id="3638d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3638d-123">-DefaultProfile</span></span>
<span data-ttu-id="3638d-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3638d-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3638d-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="3638d-125">-Name</span></span>
<span data-ttu-id="3638d-126">Bu cmdlet 'in meta veri aldığı DSC düğüm yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3638d-126">Specifies the name of the DSC node configuration for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="3638d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3638d-127">-ResourceGroupName</span></span>
<span data-ttu-id="3638d-128">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3638d-128">Specifies the name of a resource group.</span></span>
<span data-ttu-id="3638d-129">Bu cmdlet, bu parametrenin belirttiği kaynak grubundaki DSC düğüm yapılandırmalarının meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="3638d-129">This cmdlet gets metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3638d-130">-RollupStatus</span><span class="sxs-lookup"><span data-stu-id="3638d-130">-RollupStatus</span></span>
<span data-ttu-id="3638d-131">Bu cmdlet 'in aldığı DSC düğüm yapılandırmalarının toplama durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3638d-131">Specifies the rollup status of DSC node configurations that this cmdlet gets.</span></span>
<span data-ttu-id="3638d-132">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="3638d-132">Valid values are:</span></span> 
- <span data-ttu-id="3638d-133">Kötü</span><span class="sxs-lookup"><span data-stu-id="3638d-133">Bad</span></span> 
- <span data-ttu-id="3638d-134">Gerçekleştireceğiniz</span><span class="sxs-lookup"><span data-stu-id="3638d-134">Good</span></span>

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

### <span data-ttu-id="3638d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3638d-135">CommonParameters</span></span>
<span data-ttu-id="3638d-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3638d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3638d-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3638d-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3638d-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3638d-138">INPUTS</span></span>

### <span data-ttu-id="3638d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3638d-139">System.String</span></span>

## <span data-ttu-id="3638d-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3638d-140">OUTPUTS</span></span>

### <span data-ttu-id="3638d-141">Microsoft. Azure. Commands. Automation. model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="3638d-141">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="3638d-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3638d-142">NOTES</span></span>

## <span data-ttu-id="3638d-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3638d-143">RELATED LINKS</span></span>

[<span data-ttu-id="3638d-144">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="3638d-144">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)


