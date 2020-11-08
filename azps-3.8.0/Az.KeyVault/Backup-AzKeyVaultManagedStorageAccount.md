---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c01d07f9408804b229921394c24e444b2a4deb8b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938236"
---
# <span data-ttu-id="208a9-101">Backup-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="208a9-101">Backup-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="208a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="208a9-102">SYNOPSIS</span></span>
<span data-ttu-id="208a9-103">Anahtar Kasası yönetimli depolama hesabını yedekler.</span><span class="sxs-lookup"><span data-stu-id="208a9-103">Backs up a KeyVault-managed storage account.</span></span>

## <span data-ttu-id="208a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="208a9-104">SYNTAX</span></span>

### <span data-ttu-id="208a9-105">ByStorageAccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="208a9-105">ByStorageAccountName (Default)</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="208a9-106">ByStorageAccount</span><span class="sxs-lookup"><span data-stu-id="208a9-106">ByStorageAccount</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="208a9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="208a9-107">DESCRIPTION</span></span>
<span data-ttu-id="208a9-108">**Backup-Azanahtarvaultmanagedstorageaccount** cmdlet 'i, bu yönetilen depolama hesabını indirip bir dosyada saklayarak bir anahtar kasada yedekler.</span><span class="sxs-lookup"><span data-stu-id="208a9-108">The **Backup-AzKeyVaultManagedStorageAccount** cmdlet backs up a specified managed storage account in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="208a9-109">İndirilen içerik şifreli olduğundan, Azure Anahtar Kasası dışında kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="208a9-109">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="208a9-110">Bir yedeklenen depolama hesabını yedeklediğiniz abonelikteki herhangi bir anahtar kasaya geri yükleyebilirsiniz; böylece kasa aynı Azure Coğrafya 'da yer alabilir.</span><span class="sxs-lookup"><span data-stu-id="208a9-110">You can restore a backed-up storage account to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="208a9-111">Bu cmdlet 'i kullanmanın tipik nedenleri şunlardır:</span><span class="sxs-lookup"><span data-stu-id="208a9-111">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="208a9-112">Kasayı yanlışlıkla yanlışlıkla silmeniz durumunda depolama hesabının çevrimdışı bir kopyasını tutmak istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="208a9-112">You want to retain an offline copy of the storage account in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="208a9-113">Anahtar Kasası kullanarak yönetilen depolama hesabı oluşturdunuz ve şimdi nesneyi başka bir Azure bölgesine kopyalamak istiyor; böylece bu uygulamayı dağıtılmış uygulamanızın tüm örneklerinden kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="208a9-113">You created a managed storage account using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="208a9-114">**Yedek-azanahtarvaultmanagedstorageaccount** cmdlet 'ini kullanarak yönetilen depolama hesabını şifreli biçimde alın ve ardından **restore-azanahtarvaultmanagedstorageaccount** cmdlet 'ini kullanın ve ikinci bölgede bir Anahtar Kasası belirtin.</span><span class="sxs-lookup"><span data-stu-id="208a9-114">Use the **Backup-AzKeyVaultManagedStorageAccount** cmdlet to retrieve the managed storage account in encrypted format and then use the **Restore-AzKeyVaultManagedStorageAccount** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="208a9-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="208a9-115">EXAMPLES</span></span>

### <span data-ttu-id="208a9-116">Örnek 1: yönetilen depolama hesabını otomatik olarak oluşturulan dosya adıyla yedekleme</span><span class="sxs-lookup"><span data-stu-id="208a9-116">Example 1: Back up a managed storage account with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

<span data-ttu-id="208a9-117">Bu komut Mykeykasası adlı anahtar kasasından MyMSAK adlı yönetilen depolama hesabını alır ve bu yönetilen depolama hesabının yedeğini sizin için otomatik olarak adlandırılmış bir dosyaya kaydeder ve dosya adını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="208a9-117">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="208a9-118">Örnek 2: yönetilen depolama hesabını belirtilen dosya adına yedekleme</span><span class="sxs-lookup"><span data-stu-id="208a9-118">Example 2: Back up a managed storage account to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="208a9-119">Bu komut Mykeykasası adındaki anahtar kasasından MyMSAK adlı yönetilen depolama hesabını alır ve bu yönetilen depolama hesabının yedeğini Backup. blob adlı bir dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="208a9-119">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file named Backup.blob.</span></span>

### <span data-ttu-id="208a9-120">Örnek 3: önceden alınmış bir yönetilen depolama hesabını belirtilen dosya adına yedekleyin, hedef dosyanın üzerine sormadan dosyaya yazılır.</span><span class="sxs-lookup"><span data-stu-id="208a9-120">Example 3: Back up a previously retrieved managed storage account to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="208a9-121">Bu komut $msak adlı yönetilen depolama hesabının yedeğini oluşturur. $Msak adlı kasada ad. VaultName, yedek. blob adlı bir dosyaya, zaten varsa dosyanın üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="208a9-121">This command creates a backup of the managed storage account named $msak.Name in the vault named $msak.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="208a9-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="208a9-122">PARAMETERS</span></span>

### <span data-ttu-id="208a9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="208a9-123">-DefaultProfile</span></span>
<span data-ttu-id="208a9-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="208a9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="208a9-125">-Force</span><span class="sxs-lookup"><span data-stu-id="208a9-125">-Force</span></span>
<span data-ttu-id="208a9-126">Varsa, verilen dosyanın üzerine yaz</span><span class="sxs-lookup"><span data-stu-id="208a9-126">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="208a9-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="208a9-127">-InputObject</span></span>
<span data-ttu-id="208a9-128">Yedeklenecek depolama hesabı paketi, bir geri alma çağrısının çıkışından alınan ardışık düzen.</span><span class="sxs-lookup"><span data-stu-id="208a9-128">Storage account bundle to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByStorageAccount
Aliases: StorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="208a9-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="208a9-129">-Name</span></span>
<span data-ttu-id="208a9-130">Gizli ad.</span><span class="sxs-lookup"><span data-stu-id="208a9-130">Secret name.</span></span>
<span data-ttu-id="208a9-131">Cmdlet, kasa adının gizliliğini, seçili durumdaki ortamı ve gizli adı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="208a9-131">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="208a9-132">-ÇıktıDosyası</span><span class="sxs-lookup"><span data-stu-id="208a9-132">-OutputFile</span></span>
<span data-ttu-id="208a9-133">Çıktı dosyası.</span><span class="sxs-lookup"><span data-stu-id="208a9-133">Output file.</span></span>
<span data-ttu-id="208a9-134">Depolama hesabı yedeğinin depolanacağı çıkış dosyası.</span><span class="sxs-lookup"><span data-stu-id="208a9-134">The output file to store the storage account backup.</span></span>
<span data-ttu-id="208a9-135">Belirtilmezse, varsayılan bir dosya adı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="208a9-135">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="208a9-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="208a9-136">-VaultName</span></span>
<span data-ttu-id="208a9-137">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="208a9-137">Vault name.</span></span>
<span data-ttu-id="208a9-138">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="208a9-138">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="208a9-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="208a9-139">-Confirm</span></span>
<span data-ttu-id="208a9-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="208a9-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="208a9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="208a9-141">-WhatIf</span></span>
<span data-ttu-id="208a9-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="208a9-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="208a9-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="208a9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="208a9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="208a9-144">CommonParameters</span></span>
<span data-ttu-id="208a9-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="208a9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="208a9-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="208a9-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="208a9-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="208a9-147">INPUTS</span></span>

### <span data-ttu-id="208a9-148">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultmanagedstorageaccountidentityıtem</span><span class="sxs-lookup"><span data-stu-id="208a9-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="208a9-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="208a9-149">OUTPUTS</span></span>

### <span data-ttu-id="208a9-150">System. String</span><span class="sxs-lookup"><span data-stu-id="208a9-150">System.String</span></span>

## <span data-ttu-id="208a9-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="208a9-151">NOTES</span></span>

## <span data-ttu-id="208a9-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="208a9-152">RELATED LINKS</span></span>