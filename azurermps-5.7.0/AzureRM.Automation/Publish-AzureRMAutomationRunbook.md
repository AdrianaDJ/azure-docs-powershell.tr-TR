---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/publish-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
ms.openlocfilehash: 1202ecbdaaf07b9ba5704a01449784172204bf73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587705"
---
# <span data-ttu-id="14ff2-101">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="14ff2-101">Publish-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="14ff2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14ff2-102">SYNOPSIS</span></span>
<span data-ttu-id="14ff2-103">Runbook yayımlar.</span><span class="sxs-lookup"><span data-stu-id="14ff2-103">Publishes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14ff2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="14ff2-104">SYNTAX</span></span>

```
Publish-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14ff2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="14ff2-105">DESCRIPTION</span></span>
<span data-ttu-id="14ff2-106">**Publish-AzureRmAutomationRunbook** cmdlet 'ı, Azure Otomasyonu 'nun üretim ortamında kullanılmak üzere bir runbook yayımlar.</span><span class="sxs-lookup"><span data-stu-id="14ff2-106">The **Publish-AzureRmAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="14ff2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="14ff2-107">EXAMPLES</span></span>

### <span data-ttu-id="14ff2-108">Örnek 1: runbook yayımlama</span><span class="sxs-lookup"><span data-stu-id="14ff2-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="14ff2-109">Bu komut, Contoso17 adlı Azure Otomasyonu hesabında Runbk01 adındaki runbook 'u yayımlar.</span><span class="sxs-lookup"><span data-stu-id="14ff2-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="14ff2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="14ff2-110">PARAMETERS</span></span>

### <span data-ttu-id="14ff2-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="14ff2-111">-AutomationAccountName</span></span>
<span data-ttu-id="14ff2-112">Bu cmdlet 'in runbook yayımladığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="14ff2-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="14ff2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14ff2-113">-DefaultProfile</span></span>
<span data-ttu-id="14ff2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="14ff2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14ff2-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="14ff2-115">-Name</span></span>
<span data-ttu-id="14ff2-116">Bu cmdlet 'in yayımladığı runbook adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="14ff2-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14ff2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14ff2-117">-ResourceGroupName</span></span>
<span data-ttu-id="14ff2-118">Bu cmdlet 'in runbook yayımladığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="14ff2-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="14ff2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14ff2-119">CommonParameters</span></span>
<span data-ttu-id="14ff2-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="14ff2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14ff2-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14ff2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14ff2-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="14ff2-122">INPUTS</span></span>

### <span data-ttu-id="14ff2-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="14ff2-123">None</span></span>
<span data-ttu-id="14ff2-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="14ff2-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="14ff2-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="14ff2-125">OUTPUTS</span></span>

### <span data-ttu-id="14ff2-126">Microsoft. Azure. Commands. Automation. model. runbook</span><span class="sxs-lookup"><span data-stu-id="14ff2-126">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="14ff2-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="14ff2-127">NOTES</span></span>

## <span data-ttu-id="14ff2-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="14ff2-128">RELATED LINKS</span></span>

[<span data-ttu-id="14ff2-129">Dışarı aktarma-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="14ff2-129">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="14ff2-130">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="14ff2-130">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="14ff2-131">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="14ff2-131">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="14ff2-132">Yeni-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="14ff2-132">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="14ff2-133">Yeni-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="14ff2-133">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="14ff2-134">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="14ff2-134">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="14ff2-135">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="14ff2-135">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="14ff2-136">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="14ff2-136">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


