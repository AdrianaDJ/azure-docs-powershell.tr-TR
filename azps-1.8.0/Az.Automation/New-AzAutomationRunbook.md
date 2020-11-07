---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationRunbook.md
ms.openlocfilehash: bbf86c6744e064b2958acaf5fe7928d537548805
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761564"
---
# <span data-ttu-id="ca728-101">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ca728-101">New-AzAutomationRunbook</span></span>

## <span data-ttu-id="ca728-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca728-102">SYNOPSIS</span></span>
<span data-ttu-id="ca728-103">Otomasyon Runbook 'u oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ca728-103">Creates an Automation runbook.</span></span>

## <span data-ttu-id="ca728-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ca728-104">SYNTAX</span></span>

```
New-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca728-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ca728-105">DESCRIPTION</span></span>
<span data-ttu-id="ca728-106">**Yeni-AzAutomationRunbook** CMDLET 'i APS kullanarak boş bir Azure Otomasyonu runbook oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ca728-106">The **New-AzAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="ca728-107">Runbook için bir ad belirtin.</span><span class="sxs-lookup"><span data-stu-id="ca728-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="ca728-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ca728-108">EXAMPLES</span></span>

### <span data-ttu-id="ca728-109">Örnek 1: runbook oluşturma</span><span class="sxs-lookup"><span data-stu-id="ca728-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ca728-110">Bu komut, Contoso17 adlı Azure Otomasyonu hesabında Runbook02 adlı bir runbook oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ca728-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="ca728-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ca728-111">PARAMETERS</span></span>

### <span data-ttu-id="ca728-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ca728-112">-AutomationAccountName</span></span>
<span data-ttu-id="ca728-113">Bu cmdlet 'in runbook oluşturduğu Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca728-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="ca728-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca728-114">-DefaultProfile</span></span>
<span data-ttu-id="ca728-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ca728-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca728-116">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="ca728-116">-Description</span></span>
<span data-ttu-id="ca728-117">Runbook için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca728-117">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="ca728-118">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="ca728-118">-LogProgress</span></span>
<span data-ttu-id="ca728-119">Runbook 'un ilerleme durumunu günlüğe kaydetmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca728-119">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="ca728-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="ca728-120">-LogVerbose</span></span>
<span data-ttu-id="ca728-121">Günlüğün ayrıntılı bilgiler içerip içermediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca728-121">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="ca728-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="ca728-122">-Name</span></span>
<span data-ttu-id="ca728-123">Runbook için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca728-123">Specifies a name for the runbook.</span></span>

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

### <span data-ttu-id="ca728-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca728-124">-ResourceGroupName</span></span>
<span data-ttu-id="ca728-125">Bu cmdlet 'in runbook oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca728-125">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="ca728-126">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="ca728-126">-Tags</span></span>
<span data-ttu-id="ca728-127">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="ca728-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ca728-128">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="ca728-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ca728-129">-Tür</span><span class="sxs-lookup"><span data-stu-id="ca728-129">-Type</span></span>
<span data-ttu-id="ca728-130">Bu cmdlet 'in oluşturduğu runbook türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca728-130">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="ca728-131">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="ca728-131">Valid values are:</span></span>
- <span data-ttu-id="ca728-132">Tiğinin</span><span class="sxs-lookup"><span data-stu-id="ca728-132">PowerShell</span></span>
- <span data-ttu-id="ca728-133">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="ca728-133">GraphicalPowerShell</span></span>
- <span data-ttu-id="ca728-134">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="ca728-134">PowerShellWorkflow</span></span>
- <span data-ttu-id="ca728-135">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="ca728-135">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="ca728-136">Grafik</span><span class="sxs-lookup"><span data-stu-id="ca728-136">Graph</span></span>
- <span data-ttu-id="ca728-137">Python2 değer grafiği eskidir.</span><span class="sxs-lookup"><span data-stu-id="ca728-137">Python2 The value Graph is obsolete.</span></span>
<span data-ttu-id="ca728-138">GraphicalPowerShellWorkflow ile eşdeğerdir.</span><span class="sxs-lookup"><span data-stu-id="ca728-138">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph, Python2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca728-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca728-139">CommonParameters</span></span>
<span data-ttu-id="ca728-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ca728-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca728-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca728-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca728-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ca728-142">INPUTS</span></span>

### <span data-ttu-id="ca728-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ca728-143">System.String</span></span>

### <span data-ttu-id="ca728-144">System. topluluklar. IDictionary</span><span class="sxs-lookup"><span data-stu-id="ca728-144">System.Collections.IDictionary</span></span>

### <span data-ttu-id="ca728-145">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="ca728-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ca728-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ca728-146">OUTPUTS</span></span>

### <span data-ttu-id="ca728-147">Microsoft. Azure. Commands. Automation. model. runbook</span><span class="sxs-lookup"><span data-stu-id="ca728-147">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="ca728-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ca728-148">NOTES</span></span>

## <span data-ttu-id="ca728-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ca728-149">RELATED LINKS</span></span>

[<span data-ttu-id="ca728-150">Dışarı aktarma-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ca728-150">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="ca728-151">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ca728-151">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="ca728-152">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ca728-152">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="ca728-153">Yayımlama-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ca728-153">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="ca728-154">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ca728-154">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="ca728-155">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ca728-155">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="ca728-156">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ca728-156">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)
