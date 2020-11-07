---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-Azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 41fcea2b0afc7c18da2f3e4e71764bff1ab2920c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936666"
---
# <span data-ttu-id="70a95-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="70a95-101">New-AzKeyVault</span></span>

## <span data-ttu-id="70a95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70a95-102">SYNOPSIS</span></span>
<span data-ttu-id="70a95-103">Bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="70a95-103">Creates a key vault.</span></span>

## <span data-ttu-id="70a95-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="70a95-104">SYNTAX</span></span>

```
New-AzKeyVault [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete]
 [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70a95-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="70a95-105">DESCRIPTION</span></span>
<span data-ttu-id="70a95-106">**Yeni-Aztuş Kasası** cmdlet 'i, belirtilen kaynak grubunda bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="70a95-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="70a95-107">Bu cmdlet, şu anda oturum açmış olan kullanıcıya, anahtar kasasındaki anahtarları ve gizlilikleri eklemek, kaldırmak veya listelemek amacıyla izinler verir.</span><span class="sxs-lookup"><span data-stu-id="70a95-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>

<span data-ttu-id="70a95-108">Not: yeni anahtar kasayı oluşturmaya çalıştığınızda, **abonelik ' Microsoft. Keykasa ' ad alanını kullanmak için kaydedilmemiş olduğunu** görürseniz, **register-azresourceprovider-Providernamespace "Microsoft. keykasa"** öğesini çalıştırın ve ardından **New-azkeykasa** komutunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="70a95-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="70a95-109">Daha fazla bilgi için Register-AzResourceProvider konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="70a95-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="70a95-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="70a95-110">EXAMPLES</span></span>

### <span data-ttu-id="70a95-111">Örnek 1: standart bir Anahtar Kasası oluşturma</span><span class="sxs-lookup"><span data-stu-id="70a95-111">Example 1: Create a Standard key vault</span></span>
```
PS C:\>New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

<span data-ttu-id="70a95-112">Bu komut, Azure bölgesinde Contoso03Vault adlı bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="70a95-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="70a95-113">Komut, anahtar kasayı Group14 adlı kaynak grubuna ekler.</span><span class="sxs-lookup"><span data-stu-id="70a95-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="70a95-114">Komut, *SKU* parametresi için bir değer belirtmediğinden, standart bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="70a95-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="70a95-115">Örnek 2: Premium Anahtar Kasası oluşturma</span><span class="sxs-lookup"><span data-stu-id="70a95-115">Example 2: Create a Premium key vault</span></span>
```
PS C:\>New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'
```

<span data-ttu-id="70a95-116">Bu komut, önceki örnekte olduğu gibi bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="70a95-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="70a95-117">Bununla birlikte, Özel Anahtar Kasası oluşturmak için *SKU* parametresi için Premium değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="70a95-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

## <span data-ttu-id="70a95-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="70a95-118">PARAMETERS</span></span>

### <span data-ttu-id="70a95-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70a95-119">-DefaultProfile</span></span>
<span data-ttu-id="70a95-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="70a95-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70a95-121">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="70a95-121">-EnabledForDeployment</span></span>
<span data-ttu-id="70a95-122">Kaynak oluşturmada bu Anahtar Kasası, örneğin sanal makine oluştururken bu anahtar kasasına başvurulduğunda, Microsoft.</span><span class="sxs-lookup"><span data-stu-id="70a95-122">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70a95-123">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="70a95-123">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="70a95-124">Azure disk şifreleme hizmeti 'nin, bu anahtar kasasından parolaları almasını ve anahtarları kaydırılmasını sağlayın.</span><span class="sxs-lookup"><span data-stu-id="70a95-124">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70a95-125">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="70a95-125">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="70a95-126">Bu anahtar kasası bir şablon dağıtımında başvuruluyorsa, Azure Resource Manager 'ın bu anahtar kasasından gizli kod almasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="70a95-126">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70a95-127">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="70a95-127">-EnableSoftDelete</span></span>
<span data-ttu-id="70a95-128">Bu anahtar kasası için yazılımla silme işlevinin etkinleştirildiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="70a95-128">Specifies that the soft-delete functionality is enabled for this key vault.</span></span> <span data-ttu-id="70a95-129">Yazılımdan silme etkinleştirildiğinde, bir yetkisiz kullanım süresi için bu anahtar kasası ve içeriğini silindikten sonra kurtarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="70a95-129">When soft-delete is enabled, for a grace period, you can recover this key vault and its contents after it is deleted.</span></span>

<span data-ttu-id="70a95-130">Bu işlev hakkında daha fazla bilgi [için bkz.](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete)</span><span class="sxs-lookup"><span data-stu-id="70a95-130">For more information about this functionality, see [Azure Key Vault soft-delete overview](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span></span> <span data-ttu-id="70a95-131">Nasıl yapılır yönergeleri için [PowerShell Ile Anahtar Kasası kolay silme 'yi kullanma](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell)konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="70a95-131">For how-to instructions, see [How to use Key Vault soft-delete with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70a95-132">-Konum</span><span class="sxs-lookup"><span data-stu-id="70a95-132">-Location</span></span>
<span data-ttu-id="70a95-133">Anahtar Kasası oluşturacağınız Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="70a95-133">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="70a95-134">Seçimlerinizi görmek için [Get-AzureLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzureLocation) komutunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="70a95-134">Use the command [Get-AzureLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzureLocation) to see your choices.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70a95-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70a95-135">-ResourceGroupName</span></span>
<span data-ttu-id="70a95-136">Anahtar Kasası oluşturulacak varolan bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="70a95-136">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70a95-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="70a95-137">-Sku</span></span>
<span data-ttu-id="70a95-138">Anahtar Kasası örneğinin SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="70a95-138">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="70a95-139">Her SKU için hangi özelliklerin kullanılabildiği hakkında bilgi için, Azure Anahtar Kasası fiyatlandırma web sitesine ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="70a95-139">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: SkuName
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70a95-140">Etiketli</span><span class="sxs-lookup"><span data-stu-id="70a95-140">-Tag</span></span>
<span data-ttu-id="70a95-141">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="70a95-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="70a95-142">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="70a95-142">For example:</span></span>

<span data-ttu-id="70a95-143">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="70a95-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70a95-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="70a95-144">-VaultName</span></span>
<span data-ttu-id="70a95-145">Oluşturulacak Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="70a95-145">Specifies the name of the key vault to create.</span></span> <span data-ttu-id="70a95-146">Ad, harf, sayı veya kısa çizgi bileşimleri olabilir.</span><span class="sxs-lookup"><span data-stu-id="70a95-146">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="70a95-147">Ad bir harfle veya rakamla başlamalıdır ve bitmelidir.</span><span class="sxs-lookup"><span data-stu-id="70a95-147">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="70a95-148">Ad, evrensel olarak benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="70a95-148">The name must be universally unique.</span></span>

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

### <span data-ttu-id="70a95-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="70a95-149">-Confirm</span></span>
<span data-ttu-id="70a95-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="70a95-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70a95-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70a95-151">-WhatIf</span></span>
<span data-ttu-id="70a95-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="70a95-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70a95-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="70a95-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70a95-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70a95-154">CommonParameters</span></span>
<span data-ttu-id="70a95-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="70a95-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70a95-156">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70a95-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70a95-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="70a95-157">INPUTS</span></span>

### <span data-ttu-id="70a95-158">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="70a95-158">None</span></span>
<span data-ttu-id="70a95-159">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="70a95-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="70a95-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="70a95-160">OUTPUTS</span></span>

### <span data-ttu-id="70a95-161">Microsoft. Azure. Commands. Keykasa. modeller. Pskasa</span><span class="sxs-lookup"><span data-stu-id="70a95-161">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="70a95-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="70a95-162">NOTES</span></span>

## <span data-ttu-id="70a95-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="70a95-163">RELATED LINKS</span></span>

[<span data-ttu-id="70a95-164">Get-Aztuş Kasası</span><span class="sxs-lookup"><span data-stu-id="70a95-164">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="70a95-165">Remove-Aztuş Kasası</span><span class="sxs-lookup"><span data-stu-id="70a95-165">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
