---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
ms.openlocfilehash: 46c77e1538c367e38220a022bf3b84e796dd0ec3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592973"
---
# <span data-ttu-id="c7b31-101">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c7b31-101">Set-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="c7b31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7b31-102">SYNOPSIS</span></span>
<span data-ttu-id="c7b31-103">Runbook 'u değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c7b31-103">Modifies a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7b31-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c7b31-104">SYNTAX</span></span>

```
Set-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>]
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7b31-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c7b31-105">DESCRIPTION</span></span>
<span data-ttu-id="c7b31-106">**Set-AzureRmAutomationRunbook** CMDLET 'i APS 'de bir Azure Otomasyonu runbook yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c7b31-106">The **Set-AzureRmAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="c7b31-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c7b31-107">EXAMPLES</span></span>

### <span data-ttu-id="c7b31-108">Örnek 1: runbook için ayrıntılı günlüğü etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="c7b31-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c7b31-109">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki belirtilen runbook işlerinin ayrıntılı kaydını verir.</span><span class="sxs-lookup"><span data-stu-id="c7b31-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="c7b31-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c7b31-110">PARAMETERS</span></span>

### <span data-ttu-id="c7b31-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c7b31-111">-AutomationAccountName</span></span>
<span data-ttu-id="c7b31-112">Bu cmdlet 'in runbook 'u değiştirdiği Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7b31-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="c7b31-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7b31-113">-DefaultProfile</span></span>
<span data-ttu-id="c7b31-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c7b31-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7b31-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="c7b31-115">-Description</span></span>
<span data-ttu-id="c7b31-116">Runbook için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7b31-116">Specifies a description for the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7b31-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="c7b31-117">-LogProgress</span></span>
<span data-ttu-id="c7b31-118">Runbook 'un ilerleme durumunu günlüğe kaydetmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7b31-118">Specifies whether the runbook logs progress.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7b31-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="c7b31-119">-LogVerbose</span></span>
<span data-ttu-id="c7b31-120">Günlüğün ayrıntılı bilgiler içerip içermediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7b31-120">Specifies whether logging includes detailed information.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7b31-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="c7b31-121">-Name</span></span>
<span data-ttu-id="c7b31-122">Bu cmdlet 'in değiştirdiği runbook adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7b31-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c7b31-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7b31-123">-ResourceGroupName</span></span>
<span data-ttu-id="c7b31-124">Bu cmdlet 'in runbook 'u değiştirdiği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7b31-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="c7b31-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="c7b31-125">-Tag</span></span>
<span data-ttu-id="c7b31-126">Runbook etiketleri.</span><span class="sxs-lookup"><span data-stu-id="c7b31-126">The runbook tags.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7b31-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7b31-127">CommonParameters</span></span>
<span data-ttu-id="c7b31-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c7b31-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7b31-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7b31-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7b31-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c7b31-130">INPUTS</span></span>

### <span data-ttu-id="c7b31-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c7b31-131">None</span></span>
<span data-ttu-id="c7b31-132">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="c7b31-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c7b31-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c7b31-133">OUTPUTS</span></span>

### <span data-ttu-id="c7b31-134">Microsoft. Azure. Commands. Automation. model. runbook</span><span class="sxs-lookup"><span data-stu-id="c7b31-134">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="c7b31-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c7b31-135">NOTES</span></span>

## <span data-ttu-id="c7b31-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c7b31-136">RELATED LINKS</span></span>

[<span data-ttu-id="c7b31-137">Dışarı aktarma-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c7b31-137">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c7b31-138">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c7b31-138">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c7b31-139">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c7b31-139">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c7b31-140">Yeni-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c7b31-140">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c7b31-141">Yeni-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c7b31-141">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c7b31-142">Yayımlama-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c7b31-142">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c7b31-143">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c7b31-143">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c7b31-144">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c7b31-144">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


