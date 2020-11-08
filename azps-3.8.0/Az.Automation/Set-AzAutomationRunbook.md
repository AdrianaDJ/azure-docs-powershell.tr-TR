---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
ms.openlocfilehash: 0f65d59a29b06959a9763d3900a8ef07dfa517b7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938400"
---
# <span data-ttu-id="d4099-101">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d4099-101">Set-AzAutomationRunbook</span></span>

## <span data-ttu-id="d4099-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4099-102">SYNOPSIS</span></span>
<span data-ttu-id="d4099-103">Runbook 'u değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d4099-103">Modifies a runbook.</span></span>

## <span data-ttu-id="d4099-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d4099-104">SYNTAX</span></span>

```
Set-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4099-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d4099-105">DESCRIPTION</span></span>
<span data-ttu-id="d4099-106">**Set-AzAutomationRunbook** CMDLET 'i APS 'de bir Azure Otomasyonu runbook yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d4099-106">The **Set-AzAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="d4099-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d4099-107">EXAMPLES</span></span>

### <span data-ttu-id="d4099-108">Örnek 1: runbook için ayrıntılı günlüğü etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="d4099-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d4099-109">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki belirtilen runbook işlerinin ayrıntılı kaydını verir.</span><span class="sxs-lookup"><span data-stu-id="d4099-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="d4099-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d4099-110">PARAMETERS</span></span>

### <span data-ttu-id="d4099-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d4099-111">-AutomationAccountName</span></span>
<span data-ttu-id="d4099-112">Bu cmdlet 'in runbook 'u değiştirdiği Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4099-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="d4099-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4099-113">-DefaultProfile</span></span>
<span data-ttu-id="d4099-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d4099-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4099-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="d4099-115">-Description</span></span>
<span data-ttu-id="d4099-116">Runbook için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4099-116">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="d4099-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="d4099-117">-LogProgress</span></span>
<span data-ttu-id="d4099-118">Runbook 'un ilerleme durumunu günlüğe kaydetmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4099-118">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="d4099-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="d4099-119">-LogVerbose</span></span>
<span data-ttu-id="d4099-120">Günlüğün ayrıntılı bilgiler içerip içermediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4099-120">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="d4099-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="d4099-121">-Name</span></span>
<span data-ttu-id="d4099-122">Bu cmdlet 'in değiştirdiği runbook adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4099-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d4099-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4099-123">-ResourceGroupName</span></span>
<span data-ttu-id="d4099-124">Bu cmdlet 'in runbook 'u değiştirdiği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4099-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="d4099-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="d4099-125">-Tag</span></span>
<span data-ttu-id="d4099-126">Runbook etiketleri.</span><span class="sxs-lookup"><span data-stu-id="d4099-126">The runbook tags.</span></span>

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

### <span data-ttu-id="d4099-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4099-127">CommonParameters</span></span>
<span data-ttu-id="d4099-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d4099-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4099-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4099-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4099-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d4099-130">INPUTS</span></span>

### <span data-ttu-id="d4099-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d4099-131">System.String</span></span>

### <span data-ttu-id="d4099-132">System. topluluklar. IDictionary</span><span class="sxs-lookup"><span data-stu-id="d4099-132">System.Collections.IDictionary</span></span>

### <span data-ttu-id="d4099-133">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="d4099-133">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d4099-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d4099-134">OUTPUTS</span></span>

### <span data-ttu-id="d4099-135">Microsoft. Azure. Commands. Automation. model. runbook</span><span class="sxs-lookup"><span data-stu-id="d4099-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="d4099-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d4099-136">NOTES</span></span>

## <span data-ttu-id="d4099-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d4099-137">RELATED LINKS</span></span>

[<span data-ttu-id="d4099-138">Dışarı aktarma-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d4099-138">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="d4099-139">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d4099-139">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="d4099-140">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d4099-140">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="d4099-141">Yeni-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d4099-141">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="d4099-142">Yeni-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d4099-142">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="d4099-143">Yayımlama-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d4099-143">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="d4099-144">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d4099-144">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="d4099-145">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d4099-145">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)

