---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
ms.openlocfilehash: 0616cb9f2a379e93a01b450ab8a66da95ca9add1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268130"
---
# <span data-ttu-id="af26c-101">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="af26c-101">Get-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="af26c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af26c-102">SYNOPSIS</span></span>
<span data-ttu-id="af26c-103">Otomasyondan DSC yapılandırmalarını alır.</span><span class="sxs-lookup"><span data-stu-id="af26c-103">Gets DSC configurations from Automation.</span></span>

## <span data-ttu-id="af26c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af26c-104">SYNTAX</span></span>

### <span data-ttu-id="af26c-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="af26c-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af26c-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="af26c-106">ByConfigurationName</span></span>
```
Get-AzAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af26c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="af26c-107">DESCRIPTION</span></span>
<span data-ttu-id="af26c-108">**Get-AzAutomationDscConfiguration** cmdlet 'i, tüm APS</span><span class="sxs-lookup"><span data-stu-id="af26c-108">The **Get-AzAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="af26c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af26c-109">EXAMPLES</span></span>

### <span data-ttu-id="af26c-110">Örnek 1: tüm DSC yapılandırmalarını alma</span><span class="sxs-lookup"><span data-stu-id="af26c-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="af26c-111">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm DSC yapılandırmalarının meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="af26c-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="af26c-112">Örnek 2: ada göre bir DSC yapılandırması alma</span><span class="sxs-lookup"><span data-stu-id="af26c-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="af26c-113">Bu komut, Contoso17 adlı Otomasyon hesabında MyConfiguration adlı bir DSC yapılandırmasının meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="af26c-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="af26c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af26c-114">PARAMETERS</span></span>

### <span data-ttu-id="af26c-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="af26c-115">-AutomationAccountName</span></span>
<span data-ttu-id="af26c-116">Bu cmdlet 'in aldığı DSC yapılandırmalarını içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af26c-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="af26c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af26c-117">-DefaultProfile</span></span>
<span data-ttu-id="af26c-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="af26c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af26c-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="af26c-119">-Name</span></span>
<span data-ttu-id="af26c-120">Bu cmdlet 'in aldığı DSC yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af26c-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="af26c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af26c-121">-ResourceGroupName</span></span>
<span data-ttu-id="af26c-122">Bu cmdlet 'in DSC yapılandırmalarını aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af26c-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="af26c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af26c-123">CommonParameters</span></span>
<span data-ttu-id="af26c-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af26c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af26c-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af26c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af26c-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af26c-126">INPUTS</span></span>

### <span data-ttu-id="af26c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="af26c-127">System.String</span></span>

## <span data-ttu-id="af26c-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af26c-128">OUTPUTS</span></span>

### <span data-ttu-id="af26c-129">Microsoft. Azure. Commands. Automation. model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="af26c-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="af26c-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af26c-130">NOTES</span></span>

## <span data-ttu-id="af26c-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af26c-131">RELATED LINKS</span></span>

[<span data-ttu-id="af26c-132">Dışarı aktarma-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="af26c-132">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="af26c-133">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="af26c-133">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


