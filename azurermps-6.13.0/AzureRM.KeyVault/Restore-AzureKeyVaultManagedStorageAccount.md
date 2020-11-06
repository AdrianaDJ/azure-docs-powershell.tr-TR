---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 12e1844be497baa24a3b9b4aa9c4e5690564f4ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588105"
---
# <span data-ttu-id="235b9-101">Restore-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="235b9-101">Restore-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="235b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="235b9-102">SYNOPSIS</span></span>
<span data-ttu-id="235b9-103">Bir yedekleme dosyasından anahtar kasadaki yönetilen depolama hesabını geri yükler.</span><span class="sxs-lookup"><span data-stu-id="235b9-103">Restores a managed storage account in a key vault from a backup file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="235b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="235b9-104">SYNTAX</span></span>

### <span data-ttu-id="235b9-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="235b9-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="235b9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="235b9-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="235b9-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="235b9-107">ByResourceId</span></span>
```
Restore-AzureKeyVaultManagedStorageAccount [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="235b9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="235b9-108">DESCRIPTION</span></span>
<span data-ttu-id="235b9-109">**Restore-AzureKeyVaultManagedStorageAccount** cmdlet 'i, bir yedekleme dosyasından belirtilen anahtar kasasına bir yönetilen depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="235b9-109">The **Restore-AzureKeyVaultManagedStorageAccount** cmdlet creates a managed storage account in the specified key vault from a backup file.</span></span>
<span data-ttu-id="235b9-110">Bu yönetilen depolama hesabı, giriş dosyasındaki yedeklenen yönetilen depolama hesabının yinelemedir ve orijinalin adıyla aynı.</span><span class="sxs-lookup"><span data-stu-id="235b9-110">This managed storage account is a replica of the backed-up managed storage account in the input file and has the same name as the original.</span></span>
<span data-ttu-id="235b9-111">Anahtar Kasası aynı ada sahip bir yönetilen depolama hesabı içeriyorsa, orijinalin üzerine yazılması yerine bu cmdlet başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="235b9-111">If the key vault already contains a managed storage account by the same name, this cmdlet fails instead of overwriting the original.</span></span>
<span data-ttu-id="235b9-112">Yönetilen depolama hesabını geri yüklediğiniz Anahtar Kasası, yönetilen depolama hesabını yedeklediğiniz anahtar kasasından farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="235b9-112">The key vault that you restore the managed storage account into can be different from the key vault that you backed up the managed storage account from.</span></span>
<span data-ttu-id="235b9-113">Ancak, Anahtar Kasası aynı aboneliği kullanmalıdır ve aynı Coğrafya (örneğin Kuzey Amerika) bir Azure bölgesinde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="235b9-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="235b9-114"> https://azure.microsoft.com/support/trust-center/)Azure bölgelerinin coğrafi olarak eşleştirilmesi Için Microsoft Azure Güven Merkezi 'ne bakın.</span><span class="sxs-lookup"><span data-stu-id="235b9-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="235b9-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="235b9-115">EXAMPLES</span></span>

### <span data-ttu-id="235b9-116">Örnek 1: yedeklenen yönetilen depolama hesabını geri yükleme</span><span class="sxs-lookup"><span data-stu-id="235b9-116">Example 1: Restore a backed-up managed storage account</span></span>
```powershell
PS C:\> Restore-AzureKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Id                  : https://mykeyvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : MyKeyVault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="235b9-117">Bu komut, Backup. blob adındaki yedekleme dosyasındaki Mykeykasa adlı yedekleme dosyasından, tüm sürümleriyle birlikte yönetilen depolama hesabını geri yükler.</span><span class="sxs-lookup"><span data-stu-id="235b9-117">This command restores a managed storage account, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="235b9-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="235b9-118">PARAMETERS</span></span>

### <span data-ttu-id="235b9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="235b9-119">-DefaultProfile</span></span>
<span data-ttu-id="235b9-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="235b9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="235b9-121">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="235b9-121">-InputFile</span></span>
<span data-ttu-id="235b9-122">Giriş dosyası.</span><span class="sxs-lookup"><span data-stu-id="235b9-122">Input file.</span></span>
<span data-ttu-id="235b9-123">Yedeklenen blob 'u içeren giriş dosyası</span><span class="sxs-lookup"><span data-stu-id="235b9-123">The input file containing the backed-up blob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235b9-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="235b9-124">-InputObject</span></span>
<span data-ttu-id="235b9-125">Tuş Kasası nesnesi</span><span class="sxs-lookup"><span data-stu-id="235b9-125">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="235b9-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="235b9-126">-ResourceId</span></span>
<span data-ttu-id="235b9-127">Tuş Kasası kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="235b9-127">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="235b9-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="235b9-128">-VaultName</span></span>
<span data-ttu-id="235b9-129">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="235b9-129">Vault name.</span></span>
<span data-ttu-id="235b9-130">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="235b9-130">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235b9-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="235b9-131">-Confirm</span></span>
<span data-ttu-id="235b9-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="235b9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="235b9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="235b9-133">-WhatIf</span></span>
<span data-ttu-id="235b9-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="235b9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="235b9-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="235b9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="235b9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="235b9-136">CommonParameters</span></span>
<span data-ttu-id="235b9-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="235b9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="235b9-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="235b9-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="235b9-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="235b9-139">INPUTS</span></span>

### <span data-ttu-id="235b9-140">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="235b9-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="235b9-141">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="235b9-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="235b9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="235b9-142">System.String</span></span>

## <span data-ttu-id="235b9-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="235b9-143">OUTPUTS</span></span>

### <span data-ttu-id="235b9-144">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="235b9-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="235b9-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="235b9-145">NOTES</span></span>

## <span data-ttu-id="235b9-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="235b9-146">RELATED LINKS</span></span>
