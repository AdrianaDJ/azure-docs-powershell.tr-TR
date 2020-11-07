---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: b8ce1dc13204cfeeb63f5b7eb45f57e2117da511
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938821"
---
# <span data-ttu-id="dfd74-101">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="dfd74-101">Restore-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="dfd74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfd74-102">SYNOPSIS</span></span>
<span data-ttu-id="dfd74-103">Yedeklenmiş bir gizli anahtar kasası içinde gizli oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dfd74-103">Creates a secret in a key vault from a backed-up secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfd74-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dfd74-104">SYNTAX</span></span>

```
Restore-AzureKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfd74-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dfd74-105">DESCRIPTION</span></span>
<span data-ttu-id="dfd74-106">**Restore-AzureKeyVaultSecret** cmdlet 'i belirtilen anahtar kasası 'nda gizli oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dfd74-106">The **Restore-AzureKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="dfd74-107">Bu gizlilik, giriş dosyasındaki yedeklenen gizli dosyaların bir yinelemesidir ve özgün gizlilikle aynı ada sahiptir.</span><span class="sxs-lookup"><span data-stu-id="dfd74-107">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="dfd74-108">Anahtar Kasası aynı ada sahip bir gizli anahtar zaten varsa, bu cmdlet özgün gizliliğin üzerine yazılmasında başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="dfd74-108">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="dfd74-109">Yedeklemede bir parolanın birden çok sürümü varsa, tüm sürümler geri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="dfd74-109">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="dfd74-110">Parolayı geri yüklediğiniz tuş Kasası, parolayı yedeklediğiniz anahtar kasasından farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="dfd74-110">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="dfd74-111">Ancak, Anahtar Kasası aynı aboneliği kullanmalıdır ve aynı Coğrafya (örneğin Kuzey Amerika) bir Azure bölgesinde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="dfd74-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="dfd74-112"> https://azure.microsoft.com/support/trust-center/)Azure bölgelerinin coğrafi olarak eşleştirilmesi Için Microsoft Azure Güven Merkezi 'ne bakın.</span><span class="sxs-lookup"><span data-stu-id="dfd74-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="dfd74-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dfd74-113">EXAMPLES</span></span>

### <span data-ttu-id="dfd74-114">Örnek 1: yedeklenen gizliliği geri yükleme</span><span class="sxs-lookup"><span data-stu-id="dfd74-114">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzureKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="dfd74-115">Bu komut, Backup. blob adındaki yedekleme dosyasındaki Mykeykasa adlı yedekleme dosyasından, tüm sürümleri dahil bir parolayı geri yükler.</span><span class="sxs-lookup"><span data-stu-id="dfd74-115">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="dfd74-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dfd74-116">PARAMETERS</span></span>

### <span data-ttu-id="dfd74-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfd74-117">-DefaultProfile</span></span>
<span data-ttu-id="dfd74-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="dfd74-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dfd74-119">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="dfd74-119">-InputFile</span></span>
<span data-ttu-id="dfd74-120">Geri yüklenecek parolayı içeren giriş dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dfd74-120">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="dfd74-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="dfd74-121">-VaultName</span></span>
<span data-ttu-id="dfd74-122">Parolayı geri yükleyeceğiniz Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dfd74-122">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="dfd74-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="dfd74-123">-Confirm</span></span>
<span data-ttu-id="dfd74-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dfd74-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd74-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfd74-125">-WhatIf</span></span>
<span data-ttu-id="dfd74-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dfd74-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfd74-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dfd74-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd74-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfd74-128">CommonParameters</span></span>
<span data-ttu-id="dfd74-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dfd74-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfd74-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfd74-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfd74-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dfd74-131">INPUTS</span></span>

## <span data-ttu-id="dfd74-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dfd74-132">OUTPUTS</span></span>

### <span data-ttu-id="dfd74-133">Microsoft. Azure. Commands. Keykasa. modeller. Secret</span><span class="sxs-lookup"><span data-stu-id="dfd74-133">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="dfd74-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dfd74-134">NOTES</span></span>

## <span data-ttu-id="dfd74-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dfd74-135">RELATED LINKS</span></span>

[<span data-ttu-id="dfd74-136">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="dfd74-136">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="dfd74-137">Yedekleme-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="dfd74-137">Backup-AzureKeyVaultSecret</span></span>](./Backup-AzureKeyVaultSecret.md)

[<span data-ttu-id="dfd74-138">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="dfd74-138">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="dfd74-139">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="dfd74-139">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

