---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
ms.openlocfilehash: 17a39152c6e341773a2c3db7b701e0d37890f110
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937847"
---
# <span data-ttu-id="a0a06-101">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a0a06-101">Restore-AzKeyVaultKey</span></span>

## <span data-ttu-id="a0a06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0a06-102">SYNOPSIS</span></span>
<span data-ttu-id="a0a06-103">Yedeklenen anahtardan bir Anahtar Kasası 'nda anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a0a06-103">Creates a key in a key vault from a backed-up key.</span></span>

## <span data-ttu-id="a0a06-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0a06-104">SYNTAX</span></span>

### <span data-ttu-id="a0a06-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a0a06-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0a06-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a0a06-106">ByInputObject</span></span>
```
Restore-AzKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0a06-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="a0a06-107">ByResourceId</span></span>
```
Restore-AzKeyVaultKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0a06-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0a06-108">DESCRIPTION</span></span>
<span data-ttu-id="a0a06-109">**Restore-Azanahtarvaultkey** cmdlet 'i belirtilen anahtar kasası 'nda bir anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a0a06-109">The **Restore-AzKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="a0a06-110">Bu anahtar, giriş dosyasındaki yedeklenen anahtarın bir yinelemesidir ve özgün anahtarla aynı ada sahiptir.</span><span class="sxs-lookup"><span data-stu-id="a0a06-110">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="a0a06-111">Anahtar Kasası zaten aynı ada sahip bir anahtara sahipse, özgün anahtarın üzerine yazılması yerine bu cmdlet başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="a0a06-111">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="a0a06-112">Yedeklemede anahtarın birden çok sürümü varsa, tüm sürümler geri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="a0a06-112">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="a0a06-113">Anahtarı geri yüklediğiniz tuş Kasası, anahtarı yedeklediğiniz anahtar kasasından farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="a0a06-113">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="a0a06-114">Ancak, Anahtar Kasası aynı aboneliği kullanmalıdır ve aynı Coğrafya (örneğin Kuzey Amerika) bir Azure bölgesinde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a0a06-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="a0a06-115"> https://azure.microsoft.com/support/trust-center/)Azure bölgelerinin coğrafi olarak eşleştirilmesi Için Microsoft Azure Güven Merkezi 'ne bakın.</span><span class="sxs-lookup"><span data-stu-id="a0a06-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="a0a06-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0a06-116">EXAMPLES</span></span>

### <span data-ttu-id="a0a06-117">Örnek 1: Yedeklenen anahtarı geri yükleme</span><span class="sxs-lookup"><span data-stu-id="a0a06-117">Example 1: Restore a backed-up key</span></span>
```powershell
PS C:\> Restore-AzKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Vault Name     : MyKeyVault
Name           : key1
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://mykeyvault.vault.azure.net:443/keys/key1/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        :
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 4/6/2018 11:35:04 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="a0a06-118">Bu komut, Backup. blob adındaki yedekleme dosyasındaki Mykeykasa adlı bir anahtar kasasına dahil olmak üzere bir anahtarı geri yükler.</span><span class="sxs-lookup"><span data-stu-id="a0a06-118">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="a0a06-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0a06-119">PARAMETERS</span></span>

### <span data-ttu-id="a0a06-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0a06-120">-DefaultProfile</span></span>
<span data-ttu-id="a0a06-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a0a06-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0a06-122">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="a0a06-122">-InputFile</span></span>
<span data-ttu-id="a0a06-123">Geri yüklenecek anahtarın yedeğini içeren giriş dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0a06-123">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="a0a06-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0a06-124">-InputObject</span></span>
<span data-ttu-id="a0a06-125">Tuş Kasası nesnesi</span><span class="sxs-lookup"><span data-stu-id="a0a06-125">KeyVault object</span></span>

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

### <span data-ttu-id="a0a06-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a0a06-126">-ResourceId</span></span>
<span data-ttu-id="a0a06-127">Tuş Kasası kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="a0a06-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="a0a06-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a0a06-128">-VaultName</span></span>
<span data-ttu-id="a0a06-129">Anahtarın geri yükleneceği anahtar kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0a06-129">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="a0a06-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="a0a06-130">-Confirm</span></span>
<span data-ttu-id="a0a06-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a0a06-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0a06-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0a06-132">-WhatIf</span></span>
<span data-ttu-id="a0a06-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0a06-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0a06-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a0a06-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0a06-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0a06-135">CommonParameters</span></span>
<span data-ttu-id="a0a06-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0a06-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0a06-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a0a06-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0a06-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0a06-138">INPUTS</span></span>

### <span data-ttu-id="a0a06-139">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="a0a06-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="a0a06-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a0a06-140">System.String</span></span>

## <span data-ttu-id="a0a06-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0a06-141">OUTPUTS</span></span>

### <span data-ttu-id="a0a06-142">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a0a06-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="a0a06-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0a06-143">NOTES</span></span>

## <span data-ttu-id="a0a06-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0a06-144">RELATED LINKS</span></span>

[<span data-ttu-id="a0a06-145">Add-Azanahtarvaultkey</span><span class="sxs-lookup"><span data-stu-id="a0a06-145">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="a0a06-146">Yedek-Aztuş Vaultkey</span><span class="sxs-lookup"><span data-stu-id="a0a06-146">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="a0a06-147">Get-Azanahtarvaultkey</span><span class="sxs-lookup"><span data-stu-id="a0a06-147">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="a0a06-148">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a0a06-148">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)
