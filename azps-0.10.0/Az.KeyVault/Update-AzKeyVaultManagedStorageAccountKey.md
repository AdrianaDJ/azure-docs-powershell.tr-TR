---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/update-AzKeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: d73e9b02940f98db6734f851219399a2ba6c74a2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936635"
---
# <span data-ttu-id="36bd5-101">Update-AzKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="36bd5-101">Update-AzKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="36bd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36bd5-102">SYNOPSIS</span></span>
<span data-ttu-id="36bd5-103">Anahtar Kasası yönetilen Azure depolama hesabının belirtilen anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="36bd5-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="36bd5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="36bd5-104">SYNTAX</span></span>

```
Update-AzKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36bd5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="36bd5-105">DESCRIPTION</span></span>
<span data-ttu-id="36bd5-106">Anahtar Kasası yönetilen Azure depolama hesabının belirtilen anahtarını yeniden oluşturur ve anahtarı etkin anahtar olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="36bd5-106">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="36bd5-107">Anahtar Kasası proxy 'leri anahtarı yeniden oluşturmak için Azure Resource Manager 'a çağrı.</span><span class="sxs-lookup"><span data-stu-id="36bd5-107">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="36bd5-108">Arayan, verilen Azure depolama hesabında anahtarları yeniden oluşturmak için izinleri karşılamalıdır.</span><span class="sxs-lookup"><span data-stu-id="36bd5-108">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="36bd5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="36bd5-109">EXAMPLES</span></span>

### <span data-ttu-id="36bd5-110">Örnek 1: anahtarı yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="36bd5-110">Example 1: Regenerate a key</span></span>
```
PS C:\> Update-AzKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'
```

<span data-ttu-id="36bd5-111">' Mystorageaccount ' hesabının ' anahtar ' hesabını yeniden oluşturur ve ' anahtar ' değerini Anahtar Kasası yönetilen Azure depolama hesabı olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="36bd5-111">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="36bd5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="36bd5-112">PARAMETERS</span></span>

### <span data-ttu-id="36bd5-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="36bd5-113">-AccountName</span></span>
<span data-ttu-id="36bd5-114">Anahtar Kasası yönetimli depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="36bd5-114">Key Vault managed storage account name.</span></span> <span data-ttu-id="36bd5-115">Cmdlet, kasa adından yönetilen depolama hesabı adının FQDN 'sini, şu anda seçili olan ortamı ve yönetim depolama hesap adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="36bd5-115">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36bd5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36bd5-116">-DefaultProfile</span></span>
<span data-ttu-id="36bd5-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="36bd5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bd5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="36bd5-118">-Force</span></span>
<span data-ttu-id="36bd5-119">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="36bd5-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="36bd5-120">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="36bd5-120">-KeyName</span></span>
<span data-ttu-id="36bd5-121">Yeniden oluşturmak ve etkinleştirmek için depolama hesabı anahtarının adı.</span><span class="sxs-lookup"><span data-stu-id="36bd5-121">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bd5-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="36bd5-122">-PassThru</span></span>
<span data-ttu-id="36bd5-123">Cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="36bd5-123">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="36bd5-124">Bu anahtar belirtilmişse, cmdlet silinen yönetilen depolama hesabını döndürür.</span><span class="sxs-lookup"><span data-stu-id="36bd5-124">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="36bd5-125">-VaultName</span><span class="sxs-lookup"><span data-stu-id="36bd5-125">-VaultName</span></span>
<span data-ttu-id="36bd5-126">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="36bd5-126">Vault name.</span></span>
<span data-ttu-id="36bd5-127">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="36bd5-127">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="36bd5-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="36bd5-128">-Confirm</span></span>
<span data-ttu-id="36bd5-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="36bd5-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bd5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36bd5-130">-WhatIf</span></span>
<span data-ttu-id="36bd5-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="36bd5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36bd5-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="36bd5-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bd5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36bd5-133">CommonParameters</span></span>
<span data-ttu-id="36bd5-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="36bd5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36bd5-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36bd5-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36bd5-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="36bd5-136">INPUTS</span></span>

### <span data-ttu-id="36bd5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="36bd5-137">System.String</span></span>

## <span data-ttu-id="36bd5-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="36bd5-138">OUTPUTS</span></span>

### <span data-ttu-id="36bd5-139">Microsoft. Azure. Commands. Keykasa. model. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36bd5-139">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="36bd5-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="36bd5-140">NOTES</span></span>

## <span data-ttu-id="36bd5-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="36bd5-141">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

