---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultkey
schema: 2.0.0
ms.openlocfilehash: 7bad1311d463b8372d07a33c549682a2cade4041
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938822"
---
# <span data-ttu-id="bc87a-101">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bc87a-101">Restore-AzureKeyVaultKey</span></span>

## <span data-ttu-id="bc87a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc87a-102">SYNOPSIS</span></span>
<span data-ttu-id="bc87a-103">Yedeklenen anahtardan bir Anahtar Kasası 'nda anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bc87a-103">Creates a key in a key vault from a backed-up key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc87a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bc87a-104">SYNTAX</span></span>

```
Restore-AzureKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc87a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc87a-105">DESCRIPTION</span></span>
<span data-ttu-id="bc87a-106">**Restore-AzureKeyVaultKey** cmdlet 'i belirtilen anahtar kasası 'nda bir anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bc87a-106">The **Restore-AzureKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="bc87a-107">Bu anahtar, giriş dosyasındaki yedeklenen anahtarın bir yinelemesidir ve özgün anahtarla aynı ada sahiptir.</span><span class="sxs-lookup"><span data-stu-id="bc87a-107">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="bc87a-108">Anahtar Kasası zaten aynı ada sahip bir anahtara sahipse, özgün anahtarın üzerine yazılması yerine bu cmdlet başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="bc87a-108">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="bc87a-109">Yedeklemede anahtarın birden çok sürümü varsa, tüm sürümler geri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="bc87a-109">If the backup contains multiple versions of a key, all versions are restored.</span></span>

<span data-ttu-id="bc87a-110">Anahtarı geri yüklediğiniz tuş Kasası, anahtarı yedeklediğiniz anahtar kasasından farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="bc87a-110">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="bc87a-111">Ancak, Anahtar Kasası aynı aboneliği kullanmalıdır ve aynı Coğrafya (örneğin Kuzey Amerika) bir Azure bölgesinde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="bc87a-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="bc87a-112"> https://azure.microsoft.com/support/trust-center/)Azure bölgelerinin coğrafi olarak eşleştirilmesi Için Microsoft Azure Güven Merkezi 'ne bakın.</span><span class="sxs-lookup"><span data-stu-id="bc87a-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="bc87a-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bc87a-113">EXAMPLES</span></span>

### <span data-ttu-id="bc87a-114">Örnek 1: Yedeklenen anahtarı geri yükleme</span><span class="sxs-lookup"><span data-stu-id="bc87a-114">Example 1: Restore a backed-up key</span></span>
```
PS C:\>Restore-AzureKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="bc87a-115">Bu komut, Backup. blob adındaki yedekleme dosyasındaki Mykeykasa adlı bir anahtar kasasına dahil olmak üzere bir anahtarı geri yükler.</span><span class="sxs-lookup"><span data-stu-id="bc87a-115">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="bc87a-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bc87a-116">PARAMETERS</span></span>

### <span data-ttu-id="bc87a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc87a-117">-DefaultProfile</span></span>
<span data-ttu-id="bc87a-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bc87a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc87a-119">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="bc87a-119">-InputFile</span></span>
<span data-ttu-id="bc87a-120">Geri yüklenecek anahtarın yedeğini içeren giriş dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc87a-120">Specifies the input file that contains the backup of the key to restore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc87a-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="bc87a-121">-VaultName</span></span>
<span data-ttu-id="bc87a-122">Anahtarın geri yükleneceği anahtar kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc87a-122">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="bc87a-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="bc87a-123">-Confirm</span></span>
<span data-ttu-id="bc87a-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bc87a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc87a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc87a-125">-WhatIf</span></span>
<span data-ttu-id="bc87a-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bc87a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc87a-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bc87a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc87a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc87a-128">CommonParameters</span></span>
<span data-ttu-id="bc87a-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bc87a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc87a-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc87a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc87a-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bc87a-131">INPUTS</span></span>

## <span data-ttu-id="bc87a-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bc87a-132">OUTPUTS</span></span>

### <span data-ttu-id="bc87a-133">Microsoft. Azure. Commands. Keykasa. modeller. Keydemeti</span><span class="sxs-lookup"><span data-stu-id="bc87a-133">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="bc87a-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bc87a-134">NOTES</span></span>

## <span data-ttu-id="bc87a-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bc87a-135">RELATED LINKS</span></span>

[<span data-ttu-id="bc87a-136">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bc87a-136">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="bc87a-137">Yedekleme-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bc87a-137">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="bc87a-138">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bc87a-138">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="bc87a-139">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bc87a-139">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

