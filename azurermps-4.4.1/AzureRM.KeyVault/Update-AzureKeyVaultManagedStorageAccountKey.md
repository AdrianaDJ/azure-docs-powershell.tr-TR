---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: 94e1b297879e31ff42f9c12c0e4ad4a601e5e163
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593104"
---
# <span data-ttu-id="2cc2f-101">Update-AzureKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="2cc2f-101">Update-AzureKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="2cc2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cc2f-102">SYNOPSIS</span></span>
<span data-ttu-id="2cc2f-103">Anahtar Kasası yönetilen Azure depolama hesabının belirtilen anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cc2f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2cc2f-104">SYNTAX</span></span>

```
Update-AzureKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cc2f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2cc2f-105">DESCRIPTION</span></span>
<span data-ttu-id="2cc2f-106">Anahtar Kasası yönetilen Azure depolama hesabının belirtilen anahtarını yeniden oluşturur ve anahtarı etkin anahtar olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-106">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="2cc2f-107">Anahtar Kasası proxy 'leri anahtarı yeniden oluşturmak için Azure Resource Manager 'a çağrı.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-107">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="2cc2f-108">Arayan, verilen Azure depolama hesabında anahtarları yeniden oluşturmak için izinleri karşılamalıdır.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-108">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="2cc2f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2cc2f-109">EXAMPLES</span></span>

### <span data-ttu-id="2cc2f-110">Örnek 1: anahtarı yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="2cc2f-110">Example 1: Regenerate a key</span></span>
```
PS C:\> Update-AzureKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'
```

<span data-ttu-id="2cc2f-111">' Mystorageaccount ' hesabının ' anahtar ' hesabını yeniden oluşturur ve ' anahtar ' değerini Anahtar Kasası yönetilen Azure depolama hesabı olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-111">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="2cc2f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2cc2f-112">PARAMETERS</span></span>

### <span data-ttu-id="2cc2f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2cc2f-113">-AccountName</span></span>
<span data-ttu-id="2cc2f-114">Anahtar Kasası yönetimli depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-114">Key Vault managed storage account name.</span></span> <span data-ttu-id="2cc2f-115">Cmdlet, kasa adından yönetilen depolama hesabı adının FQDN 'sini, şu anda seçili olan ortamı ve yönetim depolama hesap adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-115">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cc2f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2cc2f-116">-Force</span></span>
<span data-ttu-id="2cc2f-117">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2cc2f-118">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="2cc2f-118">-KeyName</span></span>
<span data-ttu-id="2cc2f-119">Yeniden oluşturmak ve etkinleştirmek için depolama hesabı anahtarının adı.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-119">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cc2f-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2cc2f-120">-PassThru</span></span>
<span data-ttu-id="2cc2f-121">Cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-121">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="2cc2f-122">Bu anahtar belirtilmişse, cmdlet silinen yönetilen depolama hesabını döndürür.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-122">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="2cc2f-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2cc2f-123">-VaultName</span></span>
<span data-ttu-id="2cc2f-124">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-124">Vault name.</span></span>
<span data-ttu-id="2cc2f-125">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="2cc2f-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="2cc2f-126">-Confirm</span></span>
<span data-ttu-id="2cc2f-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cc2f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cc2f-128">-WhatIf</span></span>
<span data-ttu-id="2cc2f-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cc2f-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cc2f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cc2f-131">-DefaultProfile</span></span>
<span data-ttu-id="2cc2f-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cc2f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cc2f-133">CommonParameters</span></span>
<span data-ttu-id="2cc2f-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cc2f-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cc2f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cc2f-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2cc2f-136">INPUTS</span></span>

### <span data-ttu-id="2cc2f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2cc2f-137">System.String</span></span>

## <span data-ttu-id="2cc2f-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2cc2f-138">OUTPUTS</span></span>

### <span data-ttu-id="2cc2f-139">Microsoft. Azure. Commands. Keykasa. model. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2cc2f-139">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="2cc2f-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2cc2f-140">NOTES</span></span>

## <span data-ttu-id="2cc2f-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2cc2f-141">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

