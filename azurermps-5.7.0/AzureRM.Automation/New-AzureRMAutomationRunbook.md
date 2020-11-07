---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
ms.openlocfilehash: 77c089e4ab46972892a7fe9ad3cc519dc7f20551
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764190"
---
# <span data-ttu-id="18eb5-101">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="18eb5-101">New-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="18eb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18eb5-102">SYNOPSIS</span></span>
<span data-ttu-id="18eb5-103">Otomasyon Runbook 'u oluşturur.</span><span class="sxs-lookup"><span data-stu-id="18eb5-103">Creates an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18eb5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="18eb5-104">SYNTAX</span></span>

```
New-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18eb5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="18eb5-105">DESCRIPTION</span></span>
<span data-ttu-id="18eb5-106">**Yeni-AzureRmAutomationRunbook** CMDLET 'i APS kullanarak boş bir Azure Otomasyonu runbook oluşturur.</span><span class="sxs-lookup"><span data-stu-id="18eb5-106">The **New-AzureRmAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="18eb5-107">Runbook için bir ad belirtin.</span><span class="sxs-lookup"><span data-stu-id="18eb5-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="18eb5-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="18eb5-108">EXAMPLES</span></span>

### <span data-ttu-id="18eb5-109">Örnek 1: runbook oluşturma</span><span class="sxs-lookup"><span data-stu-id="18eb5-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="18eb5-110">Bu komut, Contoso17 adlı Azure Otomasyonu hesabında Runbook02 adlı bir runbook oluşturur.</span><span class="sxs-lookup"><span data-stu-id="18eb5-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="18eb5-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="18eb5-111">PARAMETERS</span></span>

### <span data-ttu-id="18eb5-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="18eb5-112">-AutomationAccountName</span></span>
<span data-ttu-id="18eb5-113">Bu cmdlet 'in runbook oluşturduğu Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18eb5-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="18eb5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18eb5-114">-DefaultProfile</span></span>
<span data-ttu-id="18eb5-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="18eb5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18eb5-116">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="18eb5-116">-Description</span></span>
<span data-ttu-id="18eb5-117">Runbook için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="18eb5-117">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="18eb5-118">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="18eb5-118">-LogProgress</span></span>
<span data-ttu-id="18eb5-119">Runbook 'un ilerleme durumunu günlüğe kaydetmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="18eb5-119">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="18eb5-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="18eb5-120">-LogVerbose</span></span>
<span data-ttu-id="18eb5-121">Günlüğün ayrıntılı bilgiler içerip içermediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="18eb5-121">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="18eb5-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="18eb5-122">-Name</span></span>
<span data-ttu-id="18eb5-123">Runbook için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="18eb5-123">Specifies a name for the runbook.</span></span>

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

### <span data-ttu-id="18eb5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18eb5-124">-ResourceGroupName</span></span>
<span data-ttu-id="18eb5-125">Bu cmdlet 'in runbook oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18eb5-125">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="18eb5-126">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="18eb5-126">-Tags</span></span>
<span data-ttu-id="18eb5-127">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="18eb5-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="18eb5-128">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="18eb5-128">For example:</span></span>

<span data-ttu-id="18eb5-129">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="18eb5-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18eb5-130">-Tür</span><span class="sxs-lookup"><span data-stu-id="18eb5-130">-Type</span></span>
<span data-ttu-id="18eb5-131">Bu cmdlet 'in oluşturduğu runbook türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="18eb5-131">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="18eb5-132">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="18eb5-132">Valid values are:</span></span>

- <span data-ttu-id="18eb5-133">Tiğinin</span><span class="sxs-lookup"><span data-stu-id="18eb5-133">PowerShell</span></span>
- <span data-ttu-id="18eb5-134">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="18eb5-134">GraphicalPowerShell</span></span>
- <span data-ttu-id="18eb5-135">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="18eb5-135">PowerShellWorkflow</span></span>
- <span data-ttu-id="18eb5-136">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="18eb5-136">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="18eb5-137">Grafik</span><span class="sxs-lookup"><span data-stu-id="18eb5-137">Graph</span></span>

<span data-ttu-id="18eb5-138">Değer grafiği eskidir.</span><span class="sxs-lookup"><span data-stu-id="18eb5-138">The value Graph is obsolete.</span></span>
<span data-ttu-id="18eb5-139">GraphicalPowerShellWorkflow ile eşdeğerdir.</span><span class="sxs-lookup"><span data-stu-id="18eb5-139">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18eb5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18eb5-140">CommonParameters</span></span>
<span data-ttu-id="18eb5-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="18eb5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18eb5-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18eb5-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18eb5-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="18eb5-143">INPUTS</span></span>

### <span data-ttu-id="18eb5-144">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="18eb5-144">None</span></span>
<span data-ttu-id="18eb5-145">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="18eb5-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="18eb5-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="18eb5-146">OUTPUTS</span></span>

### <span data-ttu-id="18eb5-147">Microsoft. Azure. Commands. Automation. model. job</span><span class="sxs-lookup"><span data-stu-id="18eb5-147">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="18eb5-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="18eb5-148">NOTES</span></span>

## <span data-ttu-id="18eb5-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="18eb5-149">RELATED LINKS</span></span>

[<span data-ttu-id="18eb5-150">Dışarı aktarma-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="18eb5-150">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="18eb5-151">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="18eb5-151">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="18eb5-152">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="18eb5-152">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="18eb5-153">Yayımlama-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="18eb5-153">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="18eb5-154">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="18eb5-154">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="18eb5-155">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="18eb5-155">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="18eb5-156">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="18eb5-156">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
