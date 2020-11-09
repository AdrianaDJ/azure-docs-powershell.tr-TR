---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
ms.openlocfilehash: 9e75b6de483f0103103434518d31b472660f4a70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319917"
---
# <span data-ttu-id="0b266-101">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0b266-101">Backup-AzManagedHsmKey</span></span>

## <span data-ttu-id="0b266-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b266-102">SYNOPSIS</span></span>
<span data-ttu-id="0b266-103">Yönetilen bir HSM 'de bir anahtarı yedekler.</span><span class="sxs-lookup"><span data-stu-id="0b266-103">Backs up a key in a managed HSM.</span></span>

## <span data-ttu-id="0b266-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b266-104">SYNTAX</span></span>

### <span data-ttu-id="0b266-105">Byanahtaradı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0b266-105">ByKeyName (Default)</span></span>
```
Backup-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b266-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="0b266-106">ByKey</span></span>
```
Backup-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b266-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b266-107">DESCRIPTION</span></span>
<span data-ttu-id="0b266-108">**Backup-AzManagedHsmKey** cmdlet 'i, YÖNETILEN bir HSM 'yi indirip bir dosyada saklayarak, belirtilen anahtarı yedekler.</span><span class="sxs-lookup"><span data-stu-id="0b266-108">The **Backup-AzManagedHsmKey** cmdlet backs up a specified key in a managed HSM by downloading it and storing it in a file.</span></span>
<span data-ttu-id="0b266-109">Anahtarın birden çok sürümü varsa, tüm sürümler yedeğe dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="0b266-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="0b266-110">İndirilen içerik şifreli olduğundan, Azure Managed HSM dışında kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="0b266-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Managed HSM.</span></span>
<span data-ttu-id="0b266-111">Yedeklenmiş bir anahtarı, yedeklediğiniz abonelikteki yönetilen HSM 'ye geri yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0b266-111">You can restore a backed-up key to any managed HSM in the subscription that it was backed up from.</span></span>
<span data-ttu-id="0b266-112">Bu cmdlet 'i kullanmanın tipik nedenleri şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0b266-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="0b266-113">Anahtarınızın bir kopyasını, yönetilen HSM 'unuzda yanlışlıkla silmeniz olasılığına karşı çevrimdışı bir kopya olmasını istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="0b266-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your managed HSM.</span></span>
 
- <span data-ttu-id="0b266-114">Yönetilen HSM 'yi kullanarak bir anahtar oluşturdunuz ve şimdi anahtarı farklı bir Azure bölgesine kopyalamak istiyorsunuz, böylece bunları Dağıtılmış uygulamanızın tüm örneklerinden kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0b266-114">You created a key using Managed HSM and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="0b266-115">Anahtarı şifreli biçimde almak için **Backup-AzManagedHsmKey** cmdlet 'ini kullanın ve sonra Restore-AzManagedHsmKey cmdlet 'ini kullanarak ikinci bölgede YÖNETILEN bir HSM belirtin.</span><span class="sxs-lookup"><span data-stu-id="0b266-115">Use the **Backup-AzManagedHsmKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzManagedHsmKey cmdlet and specify a managed HSM in the second region.</span></span>

## <span data-ttu-id="0b266-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b266-116">EXAMPLES</span></span>

### <span data-ttu-id="0b266-117">Örnek 1: otomatik olarak oluşturulan bir dosya adıyla anahtarı yedekleme</span><span class="sxs-lookup"><span data-stu-id="0b266-117">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzManagedHsmKey -HsmName testmhsm -Name testkey

C:\Users\username\testmhsm-testkey-1602664728.7106073
```

<span data-ttu-id="0b266-118">Bu komut testmhsm adındaki yönetilen HSM 'den TestKey adındaki anahtarı alır ve bu anahtarın bir yedeğini sizin için otomatik olarak adlandırılmış bir dosyaya kaydeder ve dosya adını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="0b266-118">This command retrieves the key named testkey from the managed HSM named testmhsm and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

## <span data-ttu-id="0b266-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b266-119">PARAMETERS</span></span>

### <span data-ttu-id="0b266-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b266-120">-DefaultProfile</span></span>
<span data-ttu-id="0b266-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0b266-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b266-122">-Force</span><span class="sxs-lookup"><span data-stu-id="0b266-122">-Force</span></span>
<span data-ttu-id="0b266-123">Varsa, verilen dosyanın üzerine yaz</span><span class="sxs-lookup"><span data-stu-id="0b266-123">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="0b266-124">-HsmName</span><span class="sxs-lookup"><span data-stu-id="0b266-124">-HsmName</span></span>
<span data-ttu-id="0b266-125">HSM adı.</span><span class="sxs-lookup"><span data-stu-id="0b266-125">HSM name.</span></span> <span data-ttu-id="0b266-126">Cmdlet, yönetilen bir HSM 'in FQDN 'sini ad ve şu anda seçili olan ortama göre oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b266-126">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b266-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b266-127">-InputObject</span></span>
<span data-ttu-id="0b266-128">Yedekleme için anahtar paketi, bir geri alma çağrısının çıkışından alınan ardışık düzen.</span><span class="sxs-lookup"><span data-stu-id="0b266-128">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b266-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="0b266-129">-Name</span></span>
<span data-ttu-id="0b266-130">Anahtar adı.</span><span class="sxs-lookup"><span data-stu-id="0b266-130">Key name.</span></span>
<span data-ttu-id="0b266-131">Cmdlet yönetilen HSM adından, şu anda seçili olan ortamdan ve anahtar adından bir anahtarın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b266-131">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b266-132">-ÇıktıDosyası</span><span class="sxs-lookup"><span data-stu-id="0b266-132">-OutputFile</span></span>
<span data-ttu-id="0b266-133">Çıktı dosyası.</span><span class="sxs-lookup"><span data-stu-id="0b266-133">Output file.</span></span>
<span data-ttu-id="0b266-134">Yedeklenen anahtar BLOB 'unu depolamak için çıkış dosyası.</span><span class="sxs-lookup"><span data-stu-id="0b266-134">The output file to store the backed up key blob in.</span></span>
<span data-ttu-id="0b266-135">Yoksa, varsayılan bir dosya adı seçilidir.</span><span class="sxs-lookup"><span data-stu-id="0b266-135">If not present, a default filename is chosen.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b266-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="0b266-136">-Confirm</span></span>
<span data-ttu-id="0b266-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0b266-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b266-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b266-138">-WhatIf</span></span>
<span data-ttu-id="0b266-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b266-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b266-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0b266-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b266-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b266-141">CommonParameters</span></span>
<span data-ttu-id="0b266-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b266-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b266-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0b266-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b266-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b266-144">INPUTS</span></span>

### <span data-ttu-id="0b266-145">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultkeyıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="0b266-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="0b266-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b266-146">OUTPUTS</span></span>

### <span data-ttu-id="0b266-147">System. String</span><span class="sxs-lookup"><span data-stu-id="0b266-147">System.String</span></span>

## <span data-ttu-id="0b266-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b266-148">NOTES</span></span>

## <span data-ttu-id="0b266-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b266-149">RELATED LINKS</span></span>

[<span data-ttu-id="0b266-150">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0b266-150">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="0b266-151">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0b266-151">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="0b266-152">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0b266-152">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="0b266-153">Geri al-Azmanagedhsmanahtarkaldırma</span><span class="sxs-lookup"><span data-stu-id="0b266-153">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="0b266-154">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0b266-154">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="0b266-155">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0b266-155">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)