---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 3d6d3628ba15fa4b775f4c747a29645ec0628402
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595116"
---
# <span data-ttu-id="d2b01-101">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2b01-101">Get-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="d2b01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2b01-102">SYNOPSIS</span></span>
<span data-ttu-id="d2b01-103">Otomasyondan DSC yapılandırmalarını alır.</span><span class="sxs-lookup"><span data-stu-id="d2b01-103">Gets DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2b01-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2b01-104">SYNTAX</span></span>

### <span data-ttu-id="d2b01-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d2b01-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2b01-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d2b01-106">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2b01-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d2b01-107">DESCRIPTION</span></span>
<span data-ttu-id="d2b01-108">**Get-AzureRmAutomationDscConfiguration** cmdlet 'i, Mac otomasyonundan APS Istenen durum yapılandırma (DSC) yapılandırmalarını alır.</span><span class="sxs-lookup"><span data-stu-id="d2b01-108">The **Get-AzureRmAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="d2b01-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2b01-109">EXAMPLES</span></span>

### <span data-ttu-id="d2b01-110">Örnek 1: tüm DSC yapılandırmalarını alma</span><span class="sxs-lookup"><span data-stu-id="d2b01-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="d2b01-111">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm DSC yapılandırmalarının meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="d2b01-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="d2b01-112">Örnek 2: ada göre bir DSC yapılandırması alma</span><span class="sxs-lookup"><span data-stu-id="d2b01-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="d2b01-113">Bu komut, Contoso17 adlı Otomasyon hesabında MyConfiguration adlı bir DSC yapılandırmasının meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="d2b01-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="d2b01-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2b01-114">PARAMETERS</span></span>

### <span data-ttu-id="d2b01-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d2b01-115">-AutomationAccountName</span></span>
<span data-ttu-id="d2b01-116">Bu cmdlet 'in aldığı DSC yapılandırmalarını içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2b01-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2b01-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2b01-117">-DefaultProfile</span></span>
<span data-ttu-id="d2b01-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d2b01-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2b01-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="d2b01-119">-Name</span></span>
<span data-ttu-id="d2b01-120">Bu cmdlet 'in aldığı DSC yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2b01-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByConfigurationName
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2b01-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2b01-121">-ResourceGroupName</span></span>
<span data-ttu-id="d2b01-122">Bu cmdlet 'in DSC yapılandırmalarını aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2b01-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2b01-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2b01-123">CommonParameters</span></span>
<span data-ttu-id="d2b01-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d2b01-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2b01-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2b01-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2b01-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2b01-126">INPUTS</span></span>

### <span data-ttu-id="d2b01-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d2b01-127">None</span></span>
<span data-ttu-id="d2b01-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="d2b01-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d2b01-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2b01-129">OUTPUTS</span></span>

### <span data-ttu-id="d2b01-130">Microsoft. Azure. Commands. Automation. model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2b01-130">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="d2b01-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2b01-131">NOTES</span></span>

## <span data-ttu-id="d2b01-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2b01-132">RELATED LINKS</span></span>

[<span data-ttu-id="d2b01-133">Dışarı aktarma-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2b01-133">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="d2b01-134">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2b01-134">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


