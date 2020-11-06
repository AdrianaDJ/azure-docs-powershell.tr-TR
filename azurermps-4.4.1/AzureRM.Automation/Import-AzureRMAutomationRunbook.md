---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
ms.openlocfilehash: d28166ec0a9a339017aa11bc30c0c5f0394afe94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591187"
---
# <span data-ttu-id="0c4c1-101">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0c4c1-101">Import-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="0c4c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c4c1-102">SYNOPSIS</span></span>
<span data-ttu-id="0c4c1-103">Otomasyon Runbook 'unu alır.</span><span class="sxs-lookup"><span data-stu-id="0c4c1-103">Imports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c4c1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c4c1-104">SYNTAX</span></span>

```
Import-AzureRmAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c4c1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c4c1-105">DESCRIPTION</span></span>
<span data-ttu-id="0c4c1-106">**Import-AzureRmAutomationRunbook** cmdlet 'ı bir Azure Otomasyonu runbook 'unu içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="0c4c1-106">The **Import-AzureRmAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="0c4c1-107">Wps_2 ve wps_2 Iş akışı runbook 'ları veya grafik runbook 'lar için bir grafik runbook (. graphrunbook) dosyasının içeri aktarılacağı wps_2 komut dosyası (. ps1) dosyasının yolunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="0c4c1-107">Specify the path to a wps_2 script (.ps1 ) file to import for wps_2 and wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file for graphical runbooks.</span></span> <span data-ttu-id="0c4c1-108">Dosyanın adı, runbook 'un adı olur.</span><span class="sxs-lookup"><span data-stu-id="0c4c1-108">The name of the file becomes the name of the runbook.</span></span> <span data-ttu-id="0c4c1-109">Iş akışı runbook 'ları wps_2 için, betikte dosyanın adıyla eşleşen tek bir wps_2 Iş akışı tanımı bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0c4c1-109">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="0c4c1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c4c1-110">EXAMPLES</span></span>

### <span data-ttu-id="0c4c1-111">Örnek 1: dosyadan runbook Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="0c4c1-111">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzureRmAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="0c4c1-112">İlk komut $Tags değişkenine iki anahtar/değer çifti atar.</span><span class="sxs-lookup"><span data-stu-id="0c4c1-112">The first command assigns two key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="0c4c1-113">İkinci komut, GraphicalRunbook06 adlı bir grafik runbook 'u AutomationAccount01 adlı Otomasyon hesabına aktarır.</span><span class="sxs-lookup"><span data-stu-id="0c4c1-113">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="0c4c1-114">Komut ayrıca $Tags uygulamasında depolanan etiketleri de atar.</span><span class="sxs-lookup"><span data-stu-id="0c4c1-114">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="0c4c1-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c4c1-115">PARAMETERS</span></span>

### <span data-ttu-id="0c4c1-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0c4c1-116">-AutomationAccountName</span></span>
<span data-ttu-id="0c4c1-117">Bu cmdlet 'in runbook içeri aktardıkları Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c4c1-117">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="0c4c1-118">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="0c4c1-118">-Description</span></span>
<span data-ttu-id="0c4c1-119">İçeri aktarılan runbook için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c4c1-119">Specifies a description for the imported runbook.</span></span>

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

### <span data-ttu-id="0c4c1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="0c4c1-120">-Force</span></span>
<span data-ttu-id="0c4c1-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="0c4c1-121">ps_force</span></span>

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

### <span data-ttu-id="0c4c1-122">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="0c4c1-122">-LogProgress</span></span>
<span data-ttu-id="0c4c1-123">Runbook 'un ilerleme bilgilerini günlüğe kaydedilip kaydedilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c4c1-123">Specifies whether the runbook logs progress information.</span></span>

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

### <span data-ttu-id="0c4c1-124">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="0c4c1-124">-LogVerbose</span></span>
<span data-ttu-id="0c4c1-125">Runbook 'un ayrıntılı bilgileri günlüğe kaydetmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c4c1-125">Specifies whether the runbook logs detailed information.</span></span>

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

### <span data-ttu-id="0c4c1-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="0c4c1-126">-Name</span></span>
<span data-ttu-id="0c4c1-127">Bu cmdlet 'in içeri aktardığından runbook 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c4c1-127">Specifies the name of the runbook that this cmdlet imports.</span></span>

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

### <span data-ttu-id="0c4c1-128">-Yol</span><span class="sxs-lookup"><span data-stu-id="0c4c1-128">-Path</span></span>
<span data-ttu-id="0c4c1-129">Bu cmdlet 'in içeri aktardığından bir. ps1 veya. graphrunbook dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c4c1-129">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

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

### <span data-ttu-id="0c4c1-130">Yayımlanmış</span><span class="sxs-lookup"><span data-stu-id="0c4c1-130">-Published</span></span>
<span data-ttu-id="0c4c1-131">Bu cmdlet 'in içeri aldığı runbook 'u yayımlamadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0c4c1-131">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

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

### <span data-ttu-id="0c4c1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c4c1-132">-ResourceGroupName</span></span>
<span data-ttu-id="0c4c1-133">Bu cmdlet 'in runbook aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c4c1-133">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="0c4c1-134">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="0c4c1-134">-Tags</span></span>
<span data-ttu-id="0c4c1-135">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="0c4c1-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0c4c1-136">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="0c4c1-136">For example:</span></span>

<span data-ttu-id="0c4c1-137">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="0c4c1-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0c4c1-138">-Tür</span><span class="sxs-lookup"><span data-stu-id="0c4c1-138">-Type</span></span>
<span data-ttu-id="0c4c1-139">Bu cmdlet 'in oluşturduğu runbook türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c4c1-139">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="0c4c1-140">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="0c4c1-140">Valid values are:</span></span>

- <span data-ttu-id="0c4c1-141">Tiğinin</span><span class="sxs-lookup"><span data-stu-id="0c4c1-141">PowerShell</span></span>
- <span data-ttu-id="0c4c1-142">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="0c4c1-142">GraphicalPowerShell</span></span>
- <span data-ttu-id="0c4c1-143">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="0c4c1-143">PowerShellWorkflow</span></span>
- <span data-ttu-id="0c4c1-144">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="0c4c1-144">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="0c4c1-145">Grafik</span><span class="sxs-lookup"><span data-stu-id="0c4c1-145">Graph</span></span>

<span data-ttu-id="0c4c1-146">Değer grafiği eskidir.</span><span class="sxs-lookup"><span data-stu-id="0c4c1-146">The value Graph is obsolete.</span></span>
<span data-ttu-id="0c4c1-147">GraphicalPowerShellWorkflow ile eşdeğerdir.</span><span class="sxs-lookup"><span data-stu-id="0c4c1-147">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

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

### <span data-ttu-id="0c4c1-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="0c4c1-148">-Confirm</span></span>
<span data-ttu-id="0c4c1-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0c4c1-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c4c1-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c4c1-150">-WhatIf</span></span>
<span data-ttu-id="0c4c1-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0c4c1-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c4c1-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0c4c1-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c4c1-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c4c1-153">-DefaultProfile</span></span>
<span data-ttu-id="0c4c1-154">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0c4c1-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c4c1-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c4c1-155">CommonParameters</span></span>
<span data-ttu-id="0c4c1-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c4c1-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c4c1-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c4c1-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c4c1-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c4c1-158">INPUTS</span></span>

## <span data-ttu-id="0c4c1-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c4c1-159">OUTPUTS</span></span>

### <span data-ttu-id="0c4c1-160">Microsoft. Azure. Commands. Automation. model. runbook</span><span class="sxs-lookup"><span data-stu-id="0c4c1-160">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="0c4c1-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c4c1-161">NOTES</span></span>

## <span data-ttu-id="0c4c1-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c4c1-162">RELATED LINKS</span></span>

[<span data-ttu-id="0c4c1-163">Dışarı aktarma-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0c4c1-163">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="0c4c1-164">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0c4c1-164">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="0c4c1-165">Yeni-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0c4c1-165">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="0c4c1-166">Yeni-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0c4c1-166">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="0c4c1-167">Yayımlama-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0c4c1-167">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="0c4c1-168">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0c4c1-168">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="0c4c1-169">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0c4c1-169">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="0c4c1-170">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0c4c1-170">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
