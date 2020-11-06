---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
ms.openlocfilehash: 1f7c50f0f5b11c80fce203b0c44128e380834bdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586827"
---
# <span data-ttu-id="02147-101">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="02147-101">Import-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="02147-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02147-102">SYNOPSIS</span></span>
<span data-ttu-id="02147-103">Otomasyon Runbook 'unu alır.</span><span class="sxs-lookup"><span data-stu-id="02147-103">Imports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02147-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02147-104">SYNTAX</span></span>

```
Import-AzureRmAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02147-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="02147-105">DESCRIPTION</span></span>
<span data-ttu-id="02147-106">**Import-AzureRmAutomationRunbook** cmdlet 'ı bir Azure Otomasyonu runbook 'unu içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="02147-106">The **Import-AzureRmAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="02147-107">Wps_2 ve wps_2 için Iş akışı runbook 'ları, (. graphrunbook) dosya için wps_2 (. ps1) dosya yolu belirtin</span><span class="sxs-lookup"><span data-stu-id="02147-107">Specify the path to a wps_2 script (.ps1) file to import for wps_2 and wps_2 Workflow runbooks, (.graphrunbook) file for graphical runbooks, or (.py) file for python 2 runbooks.</span></span> <span data-ttu-id="02147-108">Iş akışı runbook 'ları wps_2 için, betikte dosyanın adıyla eşleşen tek bir wps_2 Iş akışı tanımı bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="02147-108">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="02147-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02147-109">EXAMPLES</span></span>

### <span data-ttu-id="02147-110">Örnek 1: dosyadan runbook Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="02147-110">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzureRmAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="02147-111">İlk komut $Tags değişkenine iki anahtar/değer çifti atar.</span><span class="sxs-lookup"><span data-stu-id="02147-111">The first command assigns two key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="02147-112">İkinci komut, GraphicalRunbook06 adlı bir grafik runbook 'u AutomationAccount01 adlı Otomasyon hesabına aktarır.</span><span class="sxs-lookup"><span data-stu-id="02147-112">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="02147-113">Komut ayrıca $Tags uygulamasında depolanan etiketleri de atar.</span><span class="sxs-lookup"><span data-stu-id="02147-113">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="02147-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02147-114">PARAMETERS</span></span>

### <span data-ttu-id="02147-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="02147-115">-AutomationAccountName</span></span>
<span data-ttu-id="02147-116">Bu cmdlet 'in runbook içeri aktardıkları Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="02147-116">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="02147-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02147-117">-DefaultProfile</span></span>
<span data-ttu-id="02147-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="02147-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02147-119">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="02147-119">-Description</span></span>
<span data-ttu-id="02147-120">İçeri aktarılan runbook için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="02147-120">Specifies a description for the imported runbook.</span></span>

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

### <span data-ttu-id="02147-121">-Force</span><span class="sxs-lookup"><span data-stu-id="02147-121">-Force</span></span>
<span data-ttu-id="02147-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="02147-122">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02147-123">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="02147-123">-LogProgress</span></span>
<span data-ttu-id="02147-124">Runbook 'un ilerleme bilgilerini günlüğe kaydedilip kaydedilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="02147-124">Specifies whether the runbook logs progress information.</span></span>

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

### <span data-ttu-id="02147-125">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="02147-125">-LogVerbose</span></span>
<span data-ttu-id="02147-126">Runbook 'un ayrıntılı bilgileri günlüğe kaydetmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="02147-126">Specifies whether the runbook logs detailed information.</span></span>

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

### <span data-ttu-id="02147-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="02147-127">-Name</span></span>
<span data-ttu-id="02147-128">Bu cmdlet 'in içeri aktardığından runbook 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="02147-128">Specifies the name of the runbook that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02147-129">-Yol</span><span class="sxs-lookup"><span data-stu-id="02147-129">-Path</span></span>
<span data-ttu-id="02147-130">Bu cmdlet 'in içeri aktardığından bir. ps1 veya. graphrunbook dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="02147-130">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourcePath

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02147-131">Yayımlanmış</span><span class="sxs-lookup"><span data-stu-id="02147-131">-Published</span></span>
<span data-ttu-id="02147-132">Bu cmdlet 'in içeri aldığı runbook 'u yayımlamadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="02147-132">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02147-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02147-133">-ResourceGroupName</span></span>
<span data-ttu-id="02147-134">Bu cmdlet 'in runbook aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="02147-134">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="02147-135">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="02147-135">-Tags</span></span>
<span data-ttu-id="02147-136">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="02147-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="02147-137">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="02147-137">For example:</span></span>

<span data-ttu-id="02147-138">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="02147-138">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="02147-139">-Tür</span><span class="sxs-lookup"><span data-stu-id="02147-139">-Type</span></span>
<span data-ttu-id="02147-140">Bu cmdlet 'in oluşturduğu runbook türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="02147-140">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="02147-141">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="02147-141">Valid values are:</span></span>

- <span data-ttu-id="02147-142">Tiğinin</span><span class="sxs-lookup"><span data-stu-id="02147-142">PowerShell</span></span>
- <span data-ttu-id="02147-143">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="02147-143">GraphicalPowerShell</span></span>
- <span data-ttu-id="02147-144">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="02147-144">PowerShellWorkflow</span></span>
- <span data-ttu-id="02147-145">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="02147-145">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="02147-146">Grafik</span><span class="sxs-lookup"><span data-stu-id="02147-146">Graph</span></span>
- <span data-ttu-id="02147-147">Python2</span><span class="sxs-lookup"><span data-stu-id="02147-147">Python2</span></span>

<span data-ttu-id="02147-148">Değer grafiği eskidir.</span><span class="sxs-lookup"><span data-stu-id="02147-148">The value Graph is obsolete.</span></span>
<span data-ttu-id="02147-149">GraphicalPowerShellWorkflow ile eşdeğerdir.</span><span class="sxs-lookup"><span data-stu-id="02147-149">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph, Python

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02147-150">-Onay</span><span class="sxs-lookup"><span data-stu-id="02147-150">-Confirm</span></span>
<span data-ttu-id="02147-151">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="02147-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02147-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02147-152">-WhatIf</span></span>
<span data-ttu-id="02147-153">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="02147-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02147-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="02147-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02147-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02147-155">CommonParameters</span></span>
<span data-ttu-id="02147-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02147-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02147-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02147-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02147-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02147-158">INPUTS</span></span>

### <span data-ttu-id="02147-159">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="02147-159">None</span></span>
<span data-ttu-id="02147-160">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="02147-160">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="02147-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02147-161">OUTPUTS</span></span>

### <span data-ttu-id="02147-162">Microsoft. Azure. Commands. Automation. model. runbook</span><span class="sxs-lookup"><span data-stu-id="02147-162">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="02147-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02147-163">NOTES</span></span>

## <span data-ttu-id="02147-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02147-164">RELATED LINKS</span></span>

[<span data-ttu-id="02147-165">Dışarı aktarma-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="02147-165">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="02147-166">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="02147-166">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="02147-167">Yeni-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="02147-167">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="02147-168">Yeni-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="02147-168">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="02147-169">Yayımlama-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="02147-169">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="02147-170">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="02147-170">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="02147-171">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="02147-171">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="02147-172">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="02147-172">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
