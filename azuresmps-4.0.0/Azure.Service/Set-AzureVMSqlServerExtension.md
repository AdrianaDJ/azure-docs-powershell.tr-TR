---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 56C7B6F5-C2AC-4C5A-8930-645374694CC3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 053bb1bfb31b90a91d69e50b77ac6411321014f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105790"
---
# <span data-ttu-id="8dcaf-101">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="8dcaf-101">Set-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="8dcaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dcaf-102">SYNOPSIS</span></span>
<span data-ttu-id="8dcaf-103">Sanal makinede Azure SQL Server uzantısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8dcaf-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="8dcaf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8dcaf-104">SYNTAX</span></span>

### <span data-ttu-id="8dcaf-105">EnableSqlServerExtension (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8dcaf-105">EnableSqlServerExtension (Default)</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>]
 [[-AutoPatchingSettings] <AutoPatchingSettings>] [[-AutoBackupSettings] <AutoBackupSettings>]
 [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8dcaf-106">DisableSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="8dcaf-106">DisableSqlServerExtension</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Disable] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="8dcaf-107">UninstallSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="8dcaf-107">UninstallSqlServerExtension</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Uninstall]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8dcaf-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8dcaf-108">DESCRIPTION</span></span>
<span data-ttu-id="8dcaf-109">**Set-AzureVMSqlServerExtension** cmdlet 'i sanal MAKINEDE Azure SQL Server uzantısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8dcaf-109">The **Set-AzureVMSqlServerExtension** cmdlet sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="8dcaf-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8dcaf-110">EXAMPLES</span></span>

### <span data-ttu-id="8dcaf-111">Örnek 1: sanal makinede otomatik düzeltme eki uygulama ayarlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="8dcaf-111">Example 1: Set auto-patching settings on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ServiceName" -Name "VMName" | Set-AzureVMSqlServerExtension -AutoPatchingSettings $APS | Update-AzureVM
```

<span data-ttu-id="8dcaf-112">Bu komut, Azure sanal makinesinde otomatik düzeltme eki ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8dcaf-112">This command sets auto-patching settings on an Azure virtual machine.</span></span>

### <span data-ttu-id="8dcaf-113">Örnek 2: sanal makinede otomatik yedekleme ayarlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="8dcaf-113">Example 2: Set auto-backup settings on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ServiceName" -Name "VMName" | Set-AzureVMSqlServerExtension -AutoBackupSettings $ABS | Update-AzureVM
```

<span data-ttu-id="8dcaf-114">Bu komut Azure sanal makinesindeki otomatik yedekleme ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8dcaf-114">This command sets auto-backup settings on Azure virtual machine.</span></span>

### <span data-ttu-id="8dcaf-115">Örnek 3: sanal makinede SQL Server uzantısını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="8dcaf-115">Example 3: Disable an SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Set-AzureVMSqlServerExtension -Disable
```

<span data-ttu-id="8dcaf-116">Bu komut, belirli bir sanal makinede SQL Server sanal makine uzantısını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="8dcaf-116">This command disables SQL Server virtual machine extension on a given virtual machine.</span></span>

### <span data-ttu-id="8dcaf-117">Örnek 4: belirli bir sanal makinede SQL Server uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="8dcaf-117">Example 4: Uninstall an SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Set-AzureVMSqlServerExtension -Uninstall
```

<span data-ttu-id="8dcaf-118">Bu komut, VMName adındaki sanal makinede SQL Server sanal makine uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8dcaf-118">This command uninstalls a SQL Server virtual machine extension on the virtual machine named VMName.</span></span>

## <span data-ttu-id="8dcaf-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8dcaf-119">PARAMETERS</span></span>

### <span data-ttu-id="8dcaf-120">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="8dcaf-120">-AutoBackupSettings</span></span>
<span data-ttu-id="8dcaf-121">Otomatik SQL Server Yedekleme ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8dcaf-121">Specifies the automatic SQL Server backup settings.</span></span>

```yaml
Type: AutoBackupSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dcaf-122">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="8dcaf-122">-AutoPatchingSettings</span></span>
<span data-ttu-id="8dcaf-123">Otomatik SQL Server düzeltme eki ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8dcaf-123">Specifies the automatic SQL Server patching settings.</span></span>

```yaml
Type: AutoPatchingSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dcaf-124">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="8dcaf-124">-Disable</span></span>
<span data-ttu-id="8dcaf-125">Bu cmdlet 'in uzantı durumunu devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8dcaf-125">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableSqlServerExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dcaf-126">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="8dcaf-126">-InformationAction</span></span>
<span data-ttu-id="8dcaf-127">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8dcaf-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8dcaf-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8dcaf-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8dcaf-129">'A</span><span class="sxs-lookup"><span data-stu-id="8dcaf-129">Continue</span></span>
- <span data-ttu-id="8dcaf-130">Manıza</span><span class="sxs-lookup"><span data-stu-id="8dcaf-130">Ignore</span></span>
- <span data-ttu-id="8dcaf-131">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="8dcaf-131">Inquire</span></span>
- <span data-ttu-id="8dcaf-132">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="8dcaf-132">SilentlyContinue</span></span>
- <span data-ttu-id="8dcaf-133">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="8dcaf-133">Stop</span></span>
- <span data-ttu-id="8dcaf-134">Biliriz</span><span class="sxs-lookup"><span data-stu-id="8dcaf-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dcaf-135">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="8dcaf-135">-InformationVariable</span></span>
<span data-ttu-id="8dcaf-136">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="8dcaf-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dcaf-137">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="8dcaf-137">-KeyVaultCredentialSettings</span></span>
<span data-ttu-id="8dcaf-138">Anahtar kasa kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8dcaf-138">Specifies key vault credential settings.</span></span>

```yaml
Type: KeyVaultCredentialSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dcaf-139">-Profil</span><span class="sxs-lookup"><span data-stu-id="8dcaf-139">-Profile</span></span>
<span data-ttu-id="8dcaf-140">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8dcaf-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8dcaf-141">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="8dcaf-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dcaf-142">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="8dcaf-142">-ReferenceName</span></span>
<span data-ttu-id="8dcaf-143">SQL Server uzantısının başvuru adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8dcaf-143">Specifies the reference name of the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dcaf-144">-Uninstall</span><span class="sxs-lookup"><span data-stu-id="8dcaf-144">-Uninstall</span></span>
<span data-ttu-id="8dcaf-145">Bu cmdlet 'in sanal makineden SQL Server uzantısını kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8dcaf-145">Indicates that this cmdlet uninstalls the SQL Server extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallSqlServerExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dcaf-146">-Version</span><span class="sxs-lookup"><span data-stu-id="8dcaf-146">-Version</span></span>
<span data-ttu-id="8dcaf-147">Get-AzureVMSqlServerExtension ayarların alınacağı SQL Server uzantısının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8dcaf-147">Specifies the version of the SQL Server extension that Get-AzureVMSqlServerExtension retrieves settings from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dcaf-148">-VM</span><span class="sxs-lookup"><span data-stu-id="8dcaf-148">-VM</span></span>
<span data-ttu-id="8dcaf-149">Kalıcı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8dcaf-149">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8dcaf-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dcaf-150">CommonParameters</span></span>
<span data-ttu-id="8dcaf-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8dcaf-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dcaf-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dcaf-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dcaf-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8dcaf-153">INPUTS</span></span>

## <span data-ttu-id="8dcaf-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8dcaf-154">OUTPUTS</span></span>

## <span data-ttu-id="8dcaf-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8dcaf-155">NOTES</span></span>

## <span data-ttu-id="8dcaf-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8dcaf-156">RELATED LINKS</span></span>

[<span data-ttu-id="8dcaf-157">Get-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="8dcaf-157">Get-AzureVMSqlServerExtension</span></span>](./Get-AzureVMSqlServerExtension.md)

[<span data-ttu-id="8dcaf-158">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="8dcaf-158">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)


