---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 4ac549e53054d0650c0e64e45c662c6b184067b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591834"
---
# <span data-ttu-id="4ed82-101">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ed82-101">Get-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="4ed82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ed82-102">SYNOPSIS</span></span>
<span data-ttu-id="4ed82-103">Otomasyondan DSC yapılandırmalarını alır.</span><span class="sxs-lookup"><span data-stu-id="4ed82-103">Gets DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ed82-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4ed82-104">SYNTAX</span></span>

### <span data-ttu-id="4ed82-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4ed82-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ed82-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="4ed82-106">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ed82-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4ed82-107">DESCRIPTION</span></span>
<span data-ttu-id="4ed82-108">**Get-AzureRmAutomationDscConfiguration** cmdlet 'i, Mac otomasyonundan APS Istenen durum yapılandırma (DSC) yapılandırmalarını alır.</span><span class="sxs-lookup"><span data-stu-id="4ed82-108">The **Get-AzureRmAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="4ed82-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4ed82-109">EXAMPLES</span></span>

### <span data-ttu-id="4ed82-110">Örnek 1: tüm DSC yapılandırmalarını alma</span><span class="sxs-lookup"><span data-stu-id="4ed82-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="4ed82-111">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm DSC yapılandırmalarının meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="4ed82-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="4ed82-112">Örnek 2: ada göre bir DSC yapılandırması alma</span><span class="sxs-lookup"><span data-stu-id="4ed82-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="4ed82-113">Bu komut, Contoso17 adlı Otomasyon hesabında MyConfiguration adlı bir DSC yapılandırmasının meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="4ed82-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="4ed82-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4ed82-114">PARAMETERS</span></span>

### <span data-ttu-id="4ed82-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4ed82-115">-AutomationAccountName</span></span>
<span data-ttu-id="4ed82-116">Bu cmdlet 'in aldığı DSC yapılandırmalarını içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ed82-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4ed82-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="4ed82-117">-Name</span></span>
<span data-ttu-id="4ed82-118">Bu cmdlet 'in aldığı DSC yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ed82-118">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ed82-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ed82-119">-ResourceGroupName</span></span>
<span data-ttu-id="4ed82-120">Bu cmdlet 'in DSC yapılandırmalarını aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ed82-120">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="4ed82-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ed82-121">-DefaultProfile</span></span>
<span data-ttu-id="4ed82-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4ed82-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ed82-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ed82-123">CommonParameters</span></span>
<span data-ttu-id="4ed82-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4ed82-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ed82-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ed82-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ed82-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4ed82-126">INPUTS</span></span>

## <span data-ttu-id="4ed82-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4ed82-127">OUTPUTS</span></span>

### <span data-ttu-id="4ed82-128">Microsoft. Azure. Commands. Automation. model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ed82-128">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="4ed82-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4ed82-129">NOTES</span></span>

## <span data-ttu-id="4ed82-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4ed82-130">RELATED LINKS</span></span>

[<span data-ttu-id="4ed82-131">Dışarı aktarma-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ed82-131">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="4ed82-132">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ed82-132">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)

