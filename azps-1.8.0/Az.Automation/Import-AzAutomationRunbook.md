---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/import-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationRunbook.md
ms.openlocfilehash: e043496f421ec6602fea61018cbaa254192def10
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761577"
---
# <span data-ttu-id="b4c5f-101">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b4c5f-101">Import-AzAutomationRunbook</span></span>

## <span data-ttu-id="b4c5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4c5f-102">SYNOPSIS</span></span>
<span data-ttu-id="b4c5f-103">Otomasyon Runbook 'unu alır.</span><span class="sxs-lookup"><span data-stu-id="b4c5f-103">Imports an Automation runbook.</span></span>

## <span data-ttu-id="b4c5f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4c5f-104">SYNTAX</span></span>

```
Import-AzAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4c5f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4c5f-105">DESCRIPTION</span></span>
<span data-ttu-id="b4c5f-106">**Import-AzAutomationRunbook** cmdlet 'ı bir Azure Otomasyonu runbook 'unu alır.</span><span class="sxs-lookup"><span data-stu-id="b4c5f-106">The **Import-AzAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="b4c5f-107">Wps_2 ve wps_2 için Iş akışı runbook 'ları, (. graphrunbook) dosya için wps_2 (. ps1) dosya yolu belirtin</span><span class="sxs-lookup"><span data-stu-id="b4c5f-107">Specify the path to a wps_2 script (.ps1) file to import for wps_2 and wps_2 Workflow runbooks, (.graphrunbook) file for graphical runbooks, or (.py) file for python 2 runbooks.</span></span> <span data-ttu-id="b4c5f-108">Iş akışı runbook 'ları wps_2 için, betikte dosyanın adıyla eşleşen tek bir wps_2 Iş akışı tanımı bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b4c5f-108">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="b4c5f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4c5f-109">EXAMPLES</span></span>

### <span data-ttu-id="b4c5f-110">Örnek 1: dosyadan runbook Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="b4c5f-110">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="b4c5f-111">İlk komut $Tags değişkenine iki anahtar/değer çifti atar.</span><span class="sxs-lookup"><span data-stu-id="b4c5f-111">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="b4c5f-112">İkinci komut, GraphicalRunbook06 adlı bir grafik runbook 'u AutomationAccount01 adlı Otomasyon hesabına aktarır.</span><span class="sxs-lookup"><span data-stu-id="b4c5f-112">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="b4c5f-113">Komut ayrıca $Tags uygulamasında depolanan etiketleri de atar.</span><span class="sxs-lookup"><span data-stu-id="b4c5f-113">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="b4c5f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4c5f-114">PARAMETERS</span></span>

### <span data-ttu-id="b4c5f-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b4c5f-115">-AutomationAccountName</span></span>
<span data-ttu-id="b4c5f-116">Bu cmdlet 'in runbook içeri aktardıkları Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4c5f-116">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="b4c5f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4c5f-117">-DefaultProfile</span></span>
<span data-ttu-id="b4c5f-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b4c5f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4c5f-119">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="b4c5f-119">-Description</span></span>
<span data-ttu-id="b4c5f-120">İçeri aktarılan runbook için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4c5f-120">Specifies a description for the imported runbook.</span></span>

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

### <span data-ttu-id="b4c5f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b4c5f-121">-Force</span></span>
<span data-ttu-id="b4c5f-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="b4c5f-122">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4c5f-123">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="b4c5f-123">-LogProgress</span></span>
<span data-ttu-id="b4c5f-124">Runbook 'un ilerleme bilgilerini günlüğe kaydedilip kaydedilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4c5f-124">Specifies whether the runbook logs progress information.</span></span>

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

### <span data-ttu-id="b4c5f-125">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="b4c5f-125">-LogVerbose</span></span>
<span data-ttu-id="b4c5f-126">Runbook 'un ayrıntılı bilgileri günlüğe kaydetmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4c5f-126">Specifies whether the runbook logs detailed information.</span></span>

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

### <span data-ttu-id="b4c5f-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="b4c5f-127">-Name</span></span>
<span data-ttu-id="b4c5f-128">Bu cmdlet 'in içeri aktardığından runbook 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4c5f-128">Specifies the name of the runbook that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4c5f-129">-Yol</span><span class="sxs-lookup"><span data-stu-id="b4c5f-129">-Path</span></span>
<span data-ttu-id="b4c5f-130">Bu cmdlet 'in içeri aktardığından bir. ps1 veya. graphrunbook dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4c5f-130">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourcePath

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4c5f-131">Yayımlanmış</span><span class="sxs-lookup"><span data-stu-id="b4c5f-131">-Published</span></span>
<span data-ttu-id="b4c5f-132">Bu cmdlet 'in içeri aldığı runbook 'u yayımlamadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4c5f-132">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4c5f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4c5f-133">-ResourceGroupName</span></span>
<span data-ttu-id="b4c5f-134">Bu cmdlet 'in runbook aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4c5f-134">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="b4c5f-135">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="b4c5f-135">-Tags</span></span>
<span data-ttu-id="b4c5f-136">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="b4c5f-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b4c5f-137">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="b4c5f-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b4c5f-138">-Tür</span><span class="sxs-lookup"><span data-stu-id="b4c5f-138">-Type</span></span>
<span data-ttu-id="b4c5f-139">Bu cmdlet 'in oluşturduğu runbook türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4c5f-139">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="b4c5f-140">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="b4c5f-140">Valid values are:</span></span>
- <span data-ttu-id="b4c5f-141">Tiğinin</span><span class="sxs-lookup"><span data-stu-id="b4c5f-141">PowerShell</span></span>
- <span data-ttu-id="b4c5f-142">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="b4c5f-142">GraphicalPowerShell</span></span>
- <span data-ttu-id="b4c5f-143">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="b4c5f-143">PowerShellWorkflow</span></span>
- <span data-ttu-id="b4c5f-144">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="b4c5f-144">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="b4c5f-145">Grafik</span><span class="sxs-lookup"><span data-stu-id="b4c5f-145">Graph</span></span>
- <span data-ttu-id="b4c5f-146">Python2 değer grafiği eskidir.</span><span class="sxs-lookup"><span data-stu-id="b4c5f-146">Python2 The value Graph is obsolete.</span></span>
<span data-ttu-id="b4c5f-147">GraphicalPowerShellWorkflow ile eşdeğerdir.</span><span class="sxs-lookup"><span data-stu-id="b4c5f-147">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

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

### <span data-ttu-id="b4c5f-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="b4c5f-148">-Confirm</span></span>
<span data-ttu-id="b4c5f-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b4c5f-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4c5f-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4c5f-150">-WhatIf</span></span>
<span data-ttu-id="b4c5f-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4c5f-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4c5f-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b4c5f-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4c5f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4c5f-153">CommonParameters</span></span>
<span data-ttu-id="b4c5f-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4c5f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4c5f-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4c5f-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4c5f-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4c5f-156">INPUTS</span></span>

### <span data-ttu-id="b4c5f-157">System. String</span><span class="sxs-lookup"><span data-stu-id="b4c5f-157">System.String</span></span>

### <span data-ttu-id="b4c5f-158">System. topluluklar. IDictionary</span><span class="sxs-lookup"><span data-stu-id="b4c5f-158">System.Collections.IDictionary</span></span>

### <span data-ttu-id="b4c5f-159">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="b4c5f-159">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b4c5f-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4c5f-160">OUTPUTS</span></span>

### <span data-ttu-id="b4c5f-161">Microsoft. Azure. Commands. Automation. model. runbook</span><span class="sxs-lookup"><span data-stu-id="b4c5f-161">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="b4c5f-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4c5f-162">NOTES</span></span>

## <span data-ttu-id="b4c5f-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4c5f-163">RELATED LINKS</span></span>

[<span data-ttu-id="b4c5f-164">Dışarı aktarma-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b4c5f-164">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="b4c5f-165">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b4c5f-165">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="b4c5f-166">Yeni-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b4c5f-166">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="b4c5f-167">Yeni-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b4c5f-167">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="b4c5f-168">Yayımlama-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b4c5f-168">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="b4c5f-169">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b4c5f-169">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="b4c5f-170">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b4c5f-170">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="b4c5f-171">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b4c5f-171">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)
