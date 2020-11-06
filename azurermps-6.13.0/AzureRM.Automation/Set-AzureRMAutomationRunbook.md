---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
ms.openlocfilehash: 26f3214cf98e43a805aab99eb3ad1b92f289b2bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589601"
---
# <span data-ttu-id="6f824-101">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6f824-101">Set-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="6f824-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f824-102">SYNOPSIS</span></span>
<span data-ttu-id="6f824-103">Runbook 'u değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6f824-103">Modifies a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f824-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6f824-104">SYNTAX</span></span>

```
Set-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>]
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f824-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6f824-105">DESCRIPTION</span></span>
<span data-ttu-id="6f824-106">**Set-AzureRmAutomationRunbook** CMDLET 'i APS 'de bir Azure Otomasyonu runbook yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6f824-106">The **Set-AzureRmAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="6f824-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6f824-107">EXAMPLES</span></span>

### <span data-ttu-id="6f824-108">Örnek 1: runbook için ayrıntılı günlüğü etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="6f824-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6f824-109">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki belirtilen runbook işlerinin ayrıntılı kaydını verir.</span><span class="sxs-lookup"><span data-stu-id="6f824-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="6f824-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6f824-110">PARAMETERS</span></span>

### <span data-ttu-id="6f824-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6f824-111">-AutomationAccountName</span></span>
<span data-ttu-id="6f824-112">Bu cmdlet 'in runbook 'u değiştirdiği Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f824-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="6f824-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f824-113">-DefaultProfile</span></span>
<span data-ttu-id="6f824-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6f824-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f824-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="6f824-115">-Description</span></span>
<span data-ttu-id="6f824-116">Runbook için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f824-116">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="6f824-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="6f824-117">-LogProgress</span></span>
<span data-ttu-id="6f824-118">Runbook 'un ilerleme durumunu günlüğe kaydetmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f824-118">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="6f824-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="6f824-119">-LogVerbose</span></span>
<span data-ttu-id="6f824-120">Günlüğün ayrıntılı bilgiler içerip içermediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f824-120">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="6f824-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="6f824-121">-Name</span></span>
<span data-ttu-id="6f824-122">Bu cmdlet 'in değiştirdiği runbook adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f824-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="6f824-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f824-123">-ResourceGroupName</span></span>
<span data-ttu-id="6f824-124">Bu cmdlet 'in runbook 'u değiştirdiği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f824-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="6f824-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="6f824-125">-Tag</span></span>
<span data-ttu-id="6f824-126">Runbook etiketleri.</span><span class="sxs-lookup"><span data-stu-id="6f824-126">The runbook tags.</span></span>

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

### <span data-ttu-id="6f824-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f824-127">CommonParameters</span></span>
<span data-ttu-id="6f824-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6f824-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f824-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f824-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f824-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6f824-130">INPUTS</span></span>

### <span data-ttu-id="6f824-131">System. String</span><span class="sxs-lookup"><span data-stu-id="6f824-131">System.String</span></span>

### <span data-ttu-id="6f824-132">System. topluluklar. IDictionary</span><span class="sxs-lookup"><span data-stu-id="6f824-132">System.Collections.IDictionary</span></span>

### <span data-ttu-id="6f824-133">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6f824-133">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="6f824-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6f824-134">OUTPUTS</span></span>

### <span data-ttu-id="6f824-135">Microsoft. Azure. Commands. Automation. model. runbook</span><span class="sxs-lookup"><span data-stu-id="6f824-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="6f824-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6f824-136">NOTES</span></span>

## <span data-ttu-id="6f824-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6f824-137">RELATED LINKS</span></span>

[<span data-ttu-id="6f824-138">Dışarı aktarma-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6f824-138">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="6f824-139">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6f824-139">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="6f824-140">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6f824-140">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="6f824-141">Yeni-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6f824-141">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="6f824-142">Yeni-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6f824-142">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="6f824-143">Yayımlama-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6f824-143">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="6f824-144">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6f824-144">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="6f824-145">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6f824-145">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


