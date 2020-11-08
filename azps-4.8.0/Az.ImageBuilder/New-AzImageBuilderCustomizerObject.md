---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderCustomizerObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
ms.openlocfilehash: 3e67452a5d5e11fa4aa96d1b38b80a4284c21f00
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108087"
---
# <span data-ttu-id="f2477-101">New-AzImageBuilderCustomizerObject</span><span class="sxs-lookup"><span data-stu-id="f2477-101">New-AzImageBuilderCustomizerObject</span></span>

## <span data-ttu-id="f2477-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2477-102">SYNOPSIS</span></span>
<span data-ttu-id="f2477-103">Bir resim özelleştirme birimi tanımlar</span><span class="sxs-lookup"><span data-stu-id="f2477-103">Describes a unit of image customization</span></span>

## <span data-ttu-id="f2477-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f2477-104">SYNTAX</span></span>

### <span data-ttu-id="f2477-105">Shellözelleştirici (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f2477-105">ShellCustomizer (Default)</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -ShellCustomizer [-Inline <String[]>]
 [-ScriptUri <String>] [-Sha256Checksum <String>] [<CommonParameters>]
```

### <span data-ttu-id="f2477-106">Dosya Özelleştirici</span><span class="sxs-lookup"><span data-stu-id="f2477-106">FileCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -FileCustomizer [-Destination <String>]
 [-Sha256Checksum <String>] [-SourceUri <String>] [<CommonParameters>]
```

### <span data-ttu-id="f2477-107">Powershellözelleştirici</span><span class="sxs-lookup"><span data-stu-id="f2477-107">PowerShellCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -PowerShellCustomizer [-Inline <String[]>]
 [-RunElevated <Boolean>] [-ScriptUri <String>] [-Sha256Checksum <String>] [-ValidExitCode <Int32[]>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2477-108">RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="f2477-108">RestartCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -RestartCustomizer [-RestartCheckCommand <String>]
 [-RestartCommand <String>] [-RestartTimeout <String>] [<CommonParameters>]
```

### <span data-ttu-id="f2477-109">Windowsupdateözelleştirici</span><span class="sxs-lookup"><span data-stu-id="f2477-109">WindowsUpdateCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -WindowsUpdateCustomizer [-Filter <String[]>]
 [-SearchCriterion <String>] [-UpdateLimit <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="f2477-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="f2477-110">DESCRIPTION</span></span>
<span data-ttu-id="f2477-111">Bir resim özelleştirme birimi tanımlar</span><span class="sxs-lookup"><span data-stu-id="f2477-111">Describes a unit of image customization</span></span>

## <span data-ttu-id="f2477-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f2477-112">EXAMPLES</span></span>

### <span data-ttu-id="f2477-113">Örnek 1: Windows Update Özelleştirici oluşturma</span><span class="sxs-lookup"><span data-stu-id="f2477-113">Example 1: Create a windows update customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -WindowsUpdateCustomizer -Filter ("BrowseOnly", "IsInstalled") -SearchCriterion "BrowseOnly=0 and IsInstalled=0"  -UpdateLimit 100 -CustomizerName 'WindUpdate'

Name       Type          Filter                    SearchCriterion                UpdateLimit
----       ----          ------                    ---------------                -----------
WindUpdate WindowsUpdate {BrowseOnly, IsInstalled} BrowseOnly=0 and IsInstalled=0 100
```

<span data-ttu-id="f2477-114">Bu komut Windows Update Özelleştirici oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f2477-114">This command creates a windows update customizer.</span></span>

### <span data-ttu-id="f2477-115">Örnek 2: dosya Özelleştirici oluşturma</span><span class="sxs-lookup"><span data-stu-id="f2477-115">Example 2: Create a file customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -FileCustomizer -CustomizerName 'filecus' -Destination 'c:\\buildArtifacts\\index.html' -SourceUri 'https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/index.html'

Name    Type Destination                    Sha256Checksum SourceUri
----    ---- -----------                    -------------- ---------
filecus File c:\\buildArtifacts\\index.html                https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/…

```

<span data-ttu-id="f2477-116">Bu komut bir dosya Özelleştirici oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f2477-116">This command creates a file customizer.</span></span>

### <span data-ttu-id="f2477-117">Örnek 3: PowerShell Özelleştirici oluşturma</span><span class="sxs-lookup"><span data-stu-id="f2477-117">Example 3: Create a powershell customizer</span></span>
```powershell
PS C:\> $inline = @("mkdir c:\\buildActions", "echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt")
PS C:\> New-AzImageBuilderCustomizerObject -PowerShellCustomizer -CustomizerName settingUpMgmtAgtPath -RunElevated $false -Inline $inline

Name                 Type       Inline                                                                                                  RunElevated ScriptUri Sha256Checksum
----                 ----       ------                                                                                                  ----------- --------- --------------
settingUpMgmtAgtPath PowerShell {mkdir c:\\buildActions, echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt} False

```

<span data-ttu-id="f2477-118">Bu komut, PowerShell Özelleştirici oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f2477-118">This command creates a powershell customizer.</span></span>

### <span data-ttu-id="f2477-119">Örnek 4: yeniden başlatma Özelleştirici oluşturma</span><span class="sxs-lookup"><span data-stu-id="f2477-119">Example 4: Create a restart customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -RestartCustomizer -CustomizerName 'restcus' -RestartCommand 'shutdown /f /r /t 0 /c \"packer restart\"' -RestartCheckCommand 'powershell -command "& {Write-Output "restarted."}"' -RestartTimeout '10m'

Name    Type           RestartCheckCommand                                 RestartCommand                            RestartTimeout
----    ----           -------------------                                 --------------                            --------------
restcus WindowsRestart powershell -command "& {Write-Output "restarted."}" shutdown /f /r /t 0 /c \"packer restart\" 10m
```

<span data-ttu-id="f2477-120">Bu komut, yeniden başlatma Özelleştirici oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f2477-120">This command creates a restart customizer.</span></span>

### <span data-ttu-id="f2477-121">Örnek 5: kabuk Özelleştirici oluşturma</span><span class="sxs-lookup"><span data-stu-id="f2477-121">Example 5: Create a shell customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName downloadBuildArtifacts -ScriptUri "https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh" 

Name                   Type  Inline ScriptUri                                                                                                      Sha256Checksum
----                   ----  ------ ---------                                                                                                      --------------
downloadBuildArtifacts Shell        https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh
```

<span data-ttu-id="f2477-122">Bu komut, kabuk Özelleştirici oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f2477-122">This command creates a shell customizer.</span></span>

## <span data-ttu-id="f2477-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f2477-123">PARAMETERS</span></span>

### <span data-ttu-id="f2477-124">-CustomizerName</span><span class="sxs-lookup"><span data-stu-id="f2477-124">-CustomizerName</span></span>
<span data-ttu-id="f2477-125">Bu özelleştirme adımında bağlam sağlamak için kolay ad.</span><span class="sxs-lookup"><span data-stu-id="f2477-125">Friendly Name to provide context on what this customization step does.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2477-126">-Hedef</span><span class="sxs-lookup"><span data-stu-id="f2477-126">-Destination</span></span>
<span data-ttu-id="f2477-127">Dosyanın (sourceUri 'den) VM 'de yükleneceği bir dosyanın mutlak yolu (halen oluşturulmuş olan iç içe dizin yapıları ile).</span><span class="sxs-lookup"><span data-stu-id="f2477-127">The absolute path to a file (with nested directory structures already created) where the file (from sourceUri) will be uploaded to in the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2477-128">-Fileözelleştirici</span><span class="sxs-lookup"><span data-stu-id="f2477-128">-FileCustomizer</span></span>
<span data-ttu-id="f2477-129">Dosyaları VM 'lere (Linux, Windows) yükler.</span><span class="sxs-lookup"><span data-stu-id="f2477-129">Uploads files to VMs (Linux, Windows).</span></span>
<span data-ttu-id="f2477-130">Packer dosya hazırlayıcısı 'na karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="f2477-130">Corresponds to Packer file provisioner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FileCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2477-131">-Filtre</span><span class="sxs-lookup"><span data-stu-id="f2477-131">-Filter</span></span>
<span data-ttu-id="f2477-132">Uygulanacak güncelleştirmeleri seçmek için filtre dizisi.</span><span class="sxs-lookup"><span data-stu-id="f2477-132">Array of filters to select updates to apply.</span></span>
<span data-ttu-id="f2477-133">Varsayılanı (filtre yok) kullanmak için boş dizi atlayın veya belirtin.</span><span class="sxs-lookup"><span data-stu-id="f2477-133">Omit or specify empty array to use the default (no filter).</span></span>
<span data-ttu-id="f2477-134">Örnekler ve bu alanın ayrıntılı açıklaması için yukarıdaki bağlantıya bakın.</span><span class="sxs-lookup"><span data-stu-id="f2477-134">Refer to above link for examples and detailed description of this field.</span></span>

```yaml
Type: System.String[]
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2477-135">-Satır içi</span><span class="sxs-lookup"><span data-stu-id="f2477-135">-Inline</span></span>
<span data-ttu-id="f2477-136">Yürütülecek kabuk komutlarının dizisi.</span><span class="sxs-lookup"><span data-stu-id="f2477-136">Array of shell commands to execute.</span></span>

```yaml
Type: System.String[]
Parameter Sets: PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2477-137">-Powershellözelleştirici</span><span class="sxs-lookup"><span data-stu-id="f2477-137">-PowerShellCustomizer</span></span>
<span data-ttu-id="f2477-138">VM 'de belirtilen PowerShell 'i (Windows) çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="f2477-138">Runs the specified PowerShell on the VM (Windows).</span></span>
<span data-ttu-id="f2477-139">Packer PowerShell hazırlayıcısı 'na karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="f2477-139">Corresponds to Packer powershell provisioner.</span></span>
<span data-ttu-id="f2477-140">Tam olarak ' scriptUri ' veya ' inline ' belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="f2477-140">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PowerShellCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2477-141">-RestartCheckCommand</span><span class="sxs-lookup"><span data-stu-id="f2477-141">-RestartCheckCommand</span></span>
<span data-ttu-id="f2477-142">Yeniden başlatmanın başarılı olup olmadığını denetleme komutu [varsayılan: ' '].</span><span class="sxs-lookup"><span data-stu-id="f2477-142">Command to check if restart succeeded [Default: ''].</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2477-143">-RestartCommand</span><span class="sxs-lookup"><span data-stu-id="f2477-143">-RestartCommand</span></span>
<span data-ttu-id="f2477-144">Yeniden başlatmayı yürütme komutu [Default: ' Shutdown/r/f/t 0/c Packer Restart ']</span><span class="sxs-lookup"><span data-stu-id="f2477-144">Command to execute the restart [Default: 'shutdown /r /f /t 0 /c packer restart']</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2477-145">-RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="f2477-145">-RestartCustomizer</span></span>
<span data-ttu-id="f2477-146">Bir VM 'yi yeniden başlatır ve geri dönmek için bekler (Windows).</span><span class="sxs-lookup"><span data-stu-id="f2477-146">Reboots a VM and waits for it to come back online (Windows).</span></span>
<span data-ttu-id="f2477-147">Windows 'un yeniden başlatma hazırlayıcısı 'na karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="f2477-147">Corresponds to Packer windows-restart provisioner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestartCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2477-148">-RestartTimeout</span><span class="sxs-lookup"><span data-stu-id="f2477-148">-RestartTimeout</span></span>
<span data-ttu-id="f2477-149">Yeniden başlatma zaman aşımı, bir büyüklük ve birim dizesi olarak belirtildi; Örneğin, ' 5m ' (5 dakika) veya ' 2 saat) [varsayılan: ' 5m '].</span><span class="sxs-lookup"><span data-stu-id="f2477-149">Restart timeout specified as a string of magnitude and unit, e.g. '5m' (5 minutes) or '2h' (2 hours) [Default: '5m'].</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2477-150">-Runyükselmesine</span><span class="sxs-lookup"><span data-stu-id="f2477-150">-RunElevated</span></span>
<span data-ttu-id="f2477-151">Belirtilmişse, PowerShell betiği yükseltilmiş ayrıcalıklarla çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="f2477-151">If specified, the PowerShell script will be run with elevated privileges.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: PowerShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2477-152">-ScriptUri</span><span class="sxs-lookup"><span data-stu-id="f2477-152">-ScriptUri</span></span>
<span data-ttu-id="f2477-153">Özelleştirme için çalıştırılacak kabuk betiğinin URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="f2477-153">URI of the shell script to be run for customizing.</span></span>
<span data-ttu-id="f2477-154">Bir GitHub bağlantısı, Azure depolama için SAS URI 'SI olabilir.</span><span class="sxs-lookup"><span data-stu-id="f2477-154">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2477-155">-Aramaölçütü</span><span class="sxs-lookup"><span data-stu-id="f2477-155">-SearchCriterion</span></span>
<span data-ttu-id="f2477-156">Güncellemeleri arama ölçütleri.</span><span class="sxs-lookup"><span data-stu-id="f2477-156">Criteria to search updates.</span></span>
<span data-ttu-id="f2477-157">Varsayılanı (tümünü ara) kullanmak için boş dize kullanmayın veya belirtin.</span><span class="sxs-lookup"><span data-stu-id="f2477-157">Omit or specify empty string to use the default (search all).</span></span>
<span data-ttu-id="f2477-158">Örnekler ve bu alanın ayrıntılı açıklaması için yukarıdaki bağlantıya bakın.</span><span class="sxs-lookup"><span data-stu-id="f2477-158">Refer to above link for examples and detailed description of this field.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2477-159">-Sha256Checksum</span><span class="sxs-lookup"><span data-stu-id="f2477-159">-Sha256Checksum</span></span>
<span data-ttu-id="f2477-160">ScriptUri alanında sağlanan kabuk betiğinin SHA256 sağlama toplamı.</span><span class="sxs-lookup"><span data-stu-id="f2477-160">SHA256 checksum of the shell script provided in the scriptUri field.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer, PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2477-161">-Shellözelleştirici</span><span class="sxs-lookup"><span data-stu-id="f2477-161">-ShellCustomizer</span></span>
<span data-ttu-id="f2477-162">Özelleştirme aşamasında (Linux) bir kabuk betiğini çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="f2477-162">Runs a shell script during the customization phase (Linux).</span></span>
<span data-ttu-id="f2477-163">Packer kabuğu hazırlayıcısı 'na karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="f2477-163">Corresponds to Packer shell provisioner.</span></span>
<span data-ttu-id="f2477-164">Tam olarak ' scriptUri ' veya ' inline ' belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="f2477-164">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShellCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2477-165">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="f2477-165">-SourceUri</span></span>
<span data-ttu-id="f2477-166">VM 'yi özelleştirmek için karşıya yüklenecek dosyanın URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="f2477-166">The URI of the file to be uploaded for customizing the VM.</span></span>
<span data-ttu-id="f2477-167">Bir GitHub bağlantısı, Azure depolama için SAS URI 'SI olabilir.</span><span class="sxs-lookup"><span data-stu-id="f2477-167">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2477-168">-UpdateLimit</span><span class="sxs-lookup"><span data-stu-id="f2477-168">-UpdateLimit</span></span>
<span data-ttu-id="f2477-169">Bir kerede uygulanacak en fazla güncelleştirme sayısı.</span><span class="sxs-lookup"><span data-stu-id="f2477-169">Maximum number of updates to apply at a time.</span></span>
<span data-ttu-id="f2477-170">Varsayılanı (1000) kullanmak için atlayın veya 0 değerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="f2477-170">Omit or specify 0 to use the default (1000).</span></span>

```yaml
Type: System.Int32
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2477-171">-ValidExitCode</span><span class="sxs-lookup"><span data-stu-id="f2477-171">-ValidExitCode</span></span>
<span data-ttu-id="f2477-172">PowerShell betiği için geçerli çıkış kodları.</span><span class="sxs-lookup"><span data-stu-id="f2477-172">Valid exit codes for the PowerShell script.</span></span>
<span data-ttu-id="f2477-173">[Varsayılan: 0].</span><span class="sxs-lookup"><span data-stu-id="f2477-173">[Default: 0].</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: PowerShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2477-174">-Windowsupdateözelleştirici</span><span class="sxs-lookup"><span data-stu-id="f2477-174">-WindowsUpdateCustomizer</span></span>
<span data-ttu-id="f2477-175">Windows güncelleştirmelerini yükler.</span><span class="sxs-lookup"><span data-stu-id="f2477-175">Installs Windows Updates.</span></span>
<span data-ttu-id="f2477-176">Windows Update Provisioner ( https://github.com/rgl/packer-provisioner-windows-update) .</span><span class="sxs-lookup"><span data-stu-id="f2477-176">Corresponds to Packer Windows Update Provisioner (https://github.com/rgl/packer-provisioner-windows-update).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2477-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2477-177">CommonParameters</span></span>
<span data-ttu-id="f2477-178">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f2477-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2477-179">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f2477-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2477-180">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f2477-180">INPUTS</span></span>

## <span data-ttu-id="f2477-181">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f2477-181">OUTPUTS</span></span>

### <span data-ttu-id="f2477-182">Microsoft. Azure. PowerShell. cmdlet. ımagebuilder. modeller. Api20200214. ıımagetemplateözelleştirici</span><span class="sxs-lookup"><span data-stu-id="f2477-182">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer</span></span>

## <span data-ttu-id="f2477-183">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f2477-183">NOTES</span></span>

<span data-ttu-id="f2477-184">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="f2477-184">ALIASES</span></span>

## <span data-ttu-id="f2477-185">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f2477-185">RELATED LINKS</span></span>

