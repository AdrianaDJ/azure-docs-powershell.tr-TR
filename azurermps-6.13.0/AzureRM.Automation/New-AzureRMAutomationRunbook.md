---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
ms.openlocfilehash: 73945c02c5c5802e169e0868908874374080b344
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591452"
---
# <span data-ttu-id="f985f-101">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f985f-101">New-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="f985f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f985f-102">SYNOPSIS</span></span>
<span data-ttu-id="f985f-103">Otomasyon Runbook 'u oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f985f-103">Creates an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f985f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f985f-104">SYNTAX</span></span>

```
New-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f985f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f985f-105">DESCRIPTION</span></span>
<span data-ttu-id="f985f-106">**Yeni-AzureRmAutomationRunbook** CMDLET 'i APS kullanarak boş bir Azure Otomasyonu runbook oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f985f-106">The **New-AzureRmAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="f985f-107">Runbook için bir ad belirtin.</span><span class="sxs-lookup"><span data-stu-id="f985f-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="f985f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f985f-108">EXAMPLES</span></span>

### <span data-ttu-id="f985f-109">Örnek 1: runbook oluşturma</span><span class="sxs-lookup"><span data-stu-id="f985f-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f985f-110">Bu komut, Contoso17 adlı Azure Otomasyonu hesabında Runbook02 adlı bir runbook oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f985f-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="f985f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f985f-111">PARAMETERS</span></span>

### <span data-ttu-id="f985f-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f985f-112">-AutomationAccountName</span></span>
<span data-ttu-id="f985f-113">Bu cmdlet 'in runbook oluşturduğu Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f985f-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="f985f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f985f-114">-DefaultProfile</span></span>
<span data-ttu-id="f985f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f985f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f985f-116">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="f985f-116">-Description</span></span>
<span data-ttu-id="f985f-117">Runbook için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="f985f-117">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="f985f-118">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="f985f-118">-LogProgress</span></span>
<span data-ttu-id="f985f-119">Runbook 'un ilerleme durumunu günlüğe kaydetmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f985f-119">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="f985f-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="f985f-120">-LogVerbose</span></span>
<span data-ttu-id="f985f-121">Günlüğün ayrıntılı bilgiler içerip içermediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f985f-121">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="f985f-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="f985f-122">-Name</span></span>
<span data-ttu-id="f985f-123">Runbook için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="f985f-123">Specifies a name for the runbook.</span></span>

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

### <span data-ttu-id="f985f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f985f-124">-ResourceGroupName</span></span>
<span data-ttu-id="f985f-125">Bu cmdlet 'in runbook oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f985f-125">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="f985f-126">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="f985f-126">-Tags</span></span>
<span data-ttu-id="f985f-127">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="f985f-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f985f-128">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="f985f-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f985f-129">-Tür</span><span class="sxs-lookup"><span data-stu-id="f985f-129">-Type</span></span>
<span data-ttu-id="f985f-130">Bu cmdlet 'in oluşturduğu runbook türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f985f-130">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="f985f-131">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="f985f-131">Valid values are:</span></span>
- <span data-ttu-id="f985f-132">Tiğinin</span><span class="sxs-lookup"><span data-stu-id="f985f-132">PowerShell</span></span>
- <span data-ttu-id="f985f-133">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="f985f-133">GraphicalPowerShell</span></span>
- <span data-ttu-id="f985f-134">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="f985f-134">PowerShellWorkflow</span></span>
- <span data-ttu-id="f985f-135">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="f985f-135">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="f985f-136">Graph değer grafiği eskidir.</span><span class="sxs-lookup"><span data-stu-id="f985f-136">Graph The value Graph is obsolete.</span></span>
<span data-ttu-id="f985f-137">GraphicalPowerShellWorkflow ile eşdeğerdir.</span><span class="sxs-lookup"><span data-stu-id="f985f-137">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f985f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f985f-138">CommonParameters</span></span>
<span data-ttu-id="f985f-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f985f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f985f-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f985f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f985f-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f985f-141">INPUTS</span></span>

### <span data-ttu-id="f985f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f985f-142">System.String</span></span>

### <span data-ttu-id="f985f-143">System. topluluklar. IDictionary</span><span class="sxs-lookup"><span data-stu-id="f985f-143">System.Collections.IDictionary</span></span>

### <span data-ttu-id="f985f-144">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f985f-144">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="f985f-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f985f-145">OUTPUTS</span></span>

### <span data-ttu-id="f985f-146">Microsoft. Azure. Commands. Automation. model. runbook</span><span class="sxs-lookup"><span data-stu-id="f985f-146">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="f985f-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f985f-147">NOTES</span></span>

## <span data-ttu-id="f985f-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f985f-148">RELATED LINKS</span></span>

[<span data-ttu-id="f985f-149">Dışarı aktarma-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f985f-149">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f985f-150">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f985f-150">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f985f-151">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f985f-151">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f985f-152">Yayımlama-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f985f-152">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f985f-153">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f985f-153">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f985f-154">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f985f-154">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f985f-155">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f985f-155">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
