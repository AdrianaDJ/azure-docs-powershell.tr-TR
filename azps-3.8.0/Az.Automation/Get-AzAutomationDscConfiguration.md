---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
ms.openlocfilehash: 0616cb9f2a379e93a01b450ab8a66da95ca9add1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098181"
---
# <span data-ttu-id="d219f-101">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d219f-101">Get-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="d219f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d219f-102">SYNOPSIS</span></span>
<span data-ttu-id="d219f-103">Otomasyondan DSC yapılandırmalarını alır.</span><span class="sxs-lookup"><span data-stu-id="d219f-103">Gets DSC configurations from Automation.</span></span>

## <span data-ttu-id="d219f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d219f-104">SYNTAX</span></span>

### <span data-ttu-id="d219f-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d219f-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d219f-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d219f-106">ByConfigurationName</span></span>
```
Get-AzAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d219f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d219f-107">DESCRIPTION</span></span>
<span data-ttu-id="d219f-108">**Get-AzAutomationDscConfiguration** cmdlet 'i, tüm APS</span><span class="sxs-lookup"><span data-stu-id="d219f-108">The **Get-AzAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="d219f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d219f-109">EXAMPLES</span></span>

### <span data-ttu-id="d219f-110">Örnek 1: tüm DSC yapılandırmalarını alma</span><span class="sxs-lookup"><span data-stu-id="d219f-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="d219f-111">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm DSC yapılandırmalarının meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="d219f-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="d219f-112">Örnek 2: ada göre bir DSC yapılandırması alma</span><span class="sxs-lookup"><span data-stu-id="d219f-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="d219f-113">Bu komut, Contoso17 adlı Otomasyon hesabında MyConfiguration adlı bir DSC yapılandırmasının meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="d219f-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="d219f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d219f-114">PARAMETERS</span></span>

### <span data-ttu-id="d219f-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d219f-115">-AutomationAccountName</span></span>
<span data-ttu-id="d219f-116">Bu cmdlet 'in aldığı DSC yapılandırmalarını içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d219f-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d219f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d219f-117">-DefaultProfile</span></span>
<span data-ttu-id="d219f-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d219f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d219f-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="d219f-119">-Name</span></span>
<span data-ttu-id="d219f-120">Bu cmdlet 'in aldığı DSC yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d219f-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d219f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d219f-121">-ResourceGroupName</span></span>
<span data-ttu-id="d219f-122">Bu cmdlet 'in DSC yapılandırmalarını aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d219f-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="d219f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d219f-123">CommonParameters</span></span>
<span data-ttu-id="d219f-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d219f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d219f-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d219f-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d219f-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d219f-126">INPUTS</span></span>

### <span data-ttu-id="d219f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d219f-127">System.String</span></span>

## <span data-ttu-id="d219f-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d219f-128">OUTPUTS</span></span>

### <span data-ttu-id="d219f-129">Microsoft. Azure. Commands. Automation. model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d219f-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="d219f-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d219f-130">NOTES</span></span>

## <span data-ttu-id="d219f-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d219f-131">RELATED LINKS</span></span>

[<span data-ttu-id="d219f-132">Dışarı aktarma-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d219f-132">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="d219f-133">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d219f-133">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


