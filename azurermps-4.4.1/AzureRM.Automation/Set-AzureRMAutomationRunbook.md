---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
ms.openlocfilehash: 69fe223a7b574e370ed58385ed21ab2462e4420f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588306"
---
# <span data-ttu-id="d0b4a-101">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d0b4a-101">Set-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="d0b4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0b4a-102">SYNOPSIS</span></span>
<span data-ttu-id="d0b4a-103">Runbook 'u değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d0b4a-103">Modifies a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0b4a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d0b4a-104">SYNTAX</span></span>

```
Set-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>]
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0b4a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d0b4a-105">DESCRIPTION</span></span>
<span data-ttu-id="d0b4a-106">**Set-AzureRmAutomationRunbook** CMDLET 'i APS 'de bir Azure Otomasyonu runbook yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d0b4a-106">The **Set-AzureRmAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="d0b4a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d0b4a-107">EXAMPLES</span></span>

### <span data-ttu-id="d0b4a-108">Örnek 1: runbook için ayrıntılı günlüğü etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="d0b4a-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d0b4a-109">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki belirtilen runbook işlerinin ayrıntılı kaydını verir.</span><span class="sxs-lookup"><span data-stu-id="d0b4a-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="d0b4a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d0b4a-110">PARAMETERS</span></span>

### <span data-ttu-id="d0b4a-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d0b4a-111">-AutomationAccountName</span></span>
<span data-ttu-id="d0b4a-112">Bu cmdlet 'in runbook 'u değiştirdiği Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0b4a-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="d0b4a-113">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="d0b4a-113">-Description</span></span>
<span data-ttu-id="d0b4a-114">Runbook için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0b4a-114">Specifies a description for the runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0b4a-115">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="d0b4a-115">-LogProgress</span></span>
<span data-ttu-id="d0b4a-116">Runbook 'un ilerleme durumunu günlüğe kaydetmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0b4a-116">Specifies whether the runbook logs progress.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0b4a-117">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="d0b4a-117">-LogVerbose</span></span>
<span data-ttu-id="d0b4a-118">Günlüğün ayrıntılı bilgiler içerip içermediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0b4a-118">Specifies whether logging includes detailed information.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0b4a-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="d0b4a-119">-Name</span></span>
<span data-ttu-id="d0b4a-120">Bu cmdlet 'in değiştirdiği runbook adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0b4a-120">Specifies the name of the runbook that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0b4a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0b4a-121">-ResourceGroupName</span></span>
<span data-ttu-id="d0b4a-122">Bu cmdlet 'in runbook 'u değiştirdiği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0b4a-122">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="d0b4a-123">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="d0b4a-123">-Tags</span></span>
<span data-ttu-id="d0b4a-124">Değiştirilmiş runbook 'un geçerli etiketlerinin yerini alacak etiketlerin sözlüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0b4a-124">Specifies a dictionary of tags to replace the current tags of the modified runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0b4a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0b4a-125">-DefaultProfile</span></span>
<span data-ttu-id="d0b4a-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d0b4a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0b4a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0b4a-127">CommonParameters</span></span>
<span data-ttu-id="d0b4a-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d0b4a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0b4a-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0b4a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0b4a-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d0b4a-130">INPUTS</span></span>

## <span data-ttu-id="d0b4a-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d0b4a-131">OUTPUTS</span></span>

### <span data-ttu-id="d0b4a-132">Microsoft. Azure. Commands. Automation. model. runbook</span><span class="sxs-lookup"><span data-stu-id="d0b4a-132">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="d0b4a-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d0b4a-133">NOTES</span></span>

## <span data-ttu-id="d0b4a-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d0b4a-134">RELATED LINKS</span></span>

[<span data-ttu-id="d0b4a-135">Dışarı aktarma-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d0b4a-135">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="d0b4a-136">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d0b4a-136">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="d0b4a-137">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d0b4a-137">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="d0b4a-138">Yeni-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d0b4a-138">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="d0b4a-139">Yeni-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d0b4a-139">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="d0b4a-140">Yayımlama-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d0b4a-140">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="d0b4a-141">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d0b4a-141">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="d0b4a-142">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d0b4a-142">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


