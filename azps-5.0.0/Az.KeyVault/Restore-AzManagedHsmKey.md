---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmKey.md
ms.openlocfilehash: 38e0dbf124643a7d669c1787314790166e88f6a9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280201"
---
# <span data-ttu-id="b5686-101">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="b5686-101">Restore-AzManagedHsmKey</span></span>

## <span data-ttu-id="b5686-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5686-102">SYNOPSIS</span></span>
<span data-ttu-id="b5686-103">Yedeklenmiş bir anahtardan yönetilen bir HSM 'de anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5686-103">Creates a key in a managed HSM from a backed-up key.</span></span>

## <span data-ttu-id="b5686-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5686-104">SYNTAX</span></span>

### <span data-ttu-id="b5686-105">ByHsmName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b5686-105">ByHsmName (Default)</span></span>
```
Restore-AzManagedHsmKey [-HsmName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5686-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b5686-106">ByInputObject</span></span>
```
Restore-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5686-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="b5686-107">ByResourceId</span></span>
```
Restore-AzManagedHsmKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5686-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5686-108">DESCRIPTION</span></span>
<span data-ttu-id="b5686-109">**Restore-AzManagedHsmKey** cmdlet 'i BELIRTILEN yönetilen HSM 'de bir anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5686-109">The **Restore-AzManagedHsmKey** cmdlet creates a key in the specified managed HSM.</span></span>
<span data-ttu-id="b5686-110">Bu anahtar, giriş dosyasındaki yedeklenen anahtarın bir yinelemesidir ve özgün anahtarla aynı ada sahiptir.</span><span class="sxs-lookup"><span data-stu-id="b5686-110">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="b5686-111">Yönetilen HSM aynı ada sahip bir anahtara sahipse, özgün anahtarın üzerine yazılması yerine bu cmdlet başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="b5686-111">If the managed HSM already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="b5686-112">Yedeklemede anahtarın birden çok sürümü varsa, tüm sürümler geri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="b5686-112">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="b5686-113">Anahtarı geri yüklediğiniz yönetilen HSM anahtarı yedeklediğiniz yönetilen HSM 'den farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="b5686-113">The managed HSM that you restore the key into can be different from the managed HSM that you backed up the key from.</span></span>
<span data-ttu-id="b5686-114">Ancak, yönetilen HSM aynı aboneliği kullanmalıdır ve aynı Coğrafya (örneğin Kuzey Amerika) bir Azure bölgesinde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b5686-114">However, the managed HSM must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="b5686-115"> https://azure.microsoft.com/support/trust-center/)Azure bölgelerinin coğrafi olarak eşleştirilmesi Için Microsoft Azure Güven Merkezi 'ne bakın.</span><span class="sxs-lookup"><span data-stu-id="b5686-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="b5686-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5686-116">EXAMPLES</span></span>

### <span data-ttu-id="b5686-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b5686-117">Example 1</span></span>
```powershell
PS C:\> Restore-AzManagedHsmKey -HsmName testmhsm -InputFile "C:\Backup.blob"

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 7cff8510da04433b98144a3e33ad2bae
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/7cff8510da04433b98144a3e33ad2bae
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 10:13:03 AM
Updated        : 10/14/2020 10:13:03 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="b5686-118">Bu komut, yedekleme. blob adındaki yedekleme dosyasındaki testmhsm adındaki yönetilen HSM 'deki tüm sürümlerinden bir anahtar geri yükler.</span><span class="sxs-lookup"><span data-stu-id="b5686-118">This command restores a key, including all of its versions, from the backup file named Backup.blob into the managed HSM named testmhsm.</span></span>

## <span data-ttu-id="b5686-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5686-119">PARAMETERS</span></span>

### <span data-ttu-id="b5686-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5686-120">-DefaultProfile</span></span>
<span data-ttu-id="b5686-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b5686-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5686-122">-HsmName</span><span class="sxs-lookup"><span data-stu-id="b5686-122">-HsmName</span></span>
<span data-ttu-id="b5686-123">HSM adı.</span><span class="sxs-lookup"><span data-stu-id="b5686-123">HSM name.</span></span> <span data-ttu-id="b5686-124">Cmdlet, yönetilen bir HSM 'in FQDN 'sini ad ve şu anda seçili olan ortama göre oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5686-124">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHsmName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5686-125">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="b5686-125">-InputFile</span></span>
<span data-ttu-id="b5686-126">Giriş dosyası.</span><span class="sxs-lookup"><span data-stu-id="b5686-126">Input file.</span></span>
<span data-ttu-id="b5686-127">Yedeklenen blob 'u içeren giriş dosyası</span><span class="sxs-lookup"><span data-stu-id="b5686-127">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="b5686-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5686-128">-InputObject</span></span>
<span data-ttu-id="b5686-129">HSM nesnesi</span><span class="sxs-lookup"><span data-stu-id="b5686-129">HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5686-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b5686-130">-ResourceId</span></span>
<span data-ttu-id="b5686-131">HSM kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="b5686-131">HSM Resource Id</span></span>

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

### <span data-ttu-id="b5686-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="b5686-132">-Confirm</span></span>
<span data-ttu-id="b5686-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b5686-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5686-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5686-134">-WhatIf</span></span>
<span data-ttu-id="b5686-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5686-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5686-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b5686-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5686-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5686-137">CommonParameters</span></span>
<span data-ttu-id="b5686-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5686-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5686-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b5686-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5686-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5686-140">INPUTS</span></span>

### <span data-ttu-id="b5686-141">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultkeyıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="b5686-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="b5686-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b5686-142">System.String</span></span>

## <span data-ttu-id="b5686-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5686-143">OUTPUTS</span></span>

### <span data-ttu-id="b5686-144">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b5686-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="b5686-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5686-145">NOTES</span></span>

## <span data-ttu-id="b5686-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5686-146">RELATED LINKS</span></span>

[<span data-ttu-id="b5686-147">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="b5686-147">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="b5686-148">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="b5686-148">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="b5686-149">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="b5686-149">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="b5686-150">Geri al-Azmanagedhsmanahtarkaldırma</span><span class="sxs-lookup"><span data-stu-id="b5686-150">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="b5686-151">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="b5686-151">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="b5686-152">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="b5686-152">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)