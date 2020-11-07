---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurermkeyvault
schema: 2.0.0
ms.openlocfilehash: b40a37729d52cfe3b1dba691fd11724fcd0b03fb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939145"
---
# <span data-ttu-id="05bf9-101">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="05bf9-101">New-AzureRmKeyVault</span></span>

## <span data-ttu-id="05bf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05bf9-102">SYNOPSIS</span></span>
<span data-ttu-id="05bf9-103">Bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="05bf9-103">Creates a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05bf9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="05bf9-104">SYNTAX</span></span>

```
New-AzureRmKeyVault [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete]
 [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05bf9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="05bf9-105">DESCRIPTION</span></span>
<span data-ttu-id="05bf9-106">**Yeni-Azurermkeykasa** cmdlet 'i belirtilen kaynak grubunda bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="05bf9-106">The **New-AzureRmKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="05bf9-107">Bu cmdlet, şu anda oturum açmış olan kullanıcıya, anahtar kasasındaki anahtarları ve gizlilikleri eklemek, kaldırmak veya listelemek amacıyla izinler verir.</span><span class="sxs-lookup"><span data-stu-id="05bf9-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>

<span data-ttu-id="05bf9-108">Not: Bu hata, **abonelik ' Microsoft. keykasa ' ad alanını kullanacak şekilde kaydedilmediğini** görürseniz **, yeni anahtar** kasayı oluşturmaya çalıştığınızda, **register-AzureRmResourceProvider-ProviderNamespace-Providernamespace-providerın**</span><span class="sxs-lookup"><span data-stu-id="05bf9-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzureRmKeyVault** command.</span></span> <span data-ttu-id="05bf9-109">Daha fazla bilgi için Register-AzureRmResourceProvider konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="05bf9-109">For more information, see Register-AzureRmResourceProvider.</span></span>

## <span data-ttu-id="05bf9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="05bf9-110">EXAMPLES</span></span>

### <span data-ttu-id="05bf9-111">Örnek 1: standart bir Anahtar Kasası oluşturma</span><span class="sxs-lookup"><span data-stu-id="05bf9-111">Example 1: Create a Standard key vault</span></span>
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

<span data-ttu-id="05bf9-112">Bu komut, Azure bölgesinde Contoso03Vault adlı bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="05bf9-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="05bf9-113">Komut, anahtar kasayı Group14 adlı kaynak grubuna ekler.</span><span class="sxs-lookup"><span data-stu-id="05bf9-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="05bf9-114">Komut, *SKU* parametresi için bir değer belirtmediğinden, standart bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="05bf9-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="05bf9-115">Örnek 2: Premium Anahtar Kasası oluşturma</span><span class="sxs-lookup"><span data-stu-id="05bf9-115">Example 2: Create a Premium key vault</span></span>
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'
```

<span data-ttu-id="05bf9-116">Bu komut, önceki örnekte olduğu gibi bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="05bf9-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="05bf9-117">Bununla birlikte, Özel Anahtar Kasası oluşturmak için *SKU* parametresi için Premium değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="05bf9-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

## <span data-ttu-id="05bf9-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="05bf9-118">PARAMETERS</span></span>

### <span data-ttu-id="05bf9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05bf9-119">-DefaultProfile</span></span>
<span data-ttu-id="05bf9-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="05bf9-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05bf9-121">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="05bf9-121">-EnabledForDeployment</span></span>
<span data-ttu-id="05bf9-122">Kaynak oluşturmada bu Anahtar Kasası, örneğin sanal makine oluştururken bu anahtar kasasına başvurulduğunda, Microsoft.</span><span class="sxs-lookup"><span data-stu-id="05bf9-122">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="05bf9-123">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="05bf9-123">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="05bf9-124">Azure disk şifreleme hizmeti 'nin, bu anahtar kasasından parolaları almasını ve anahtarları kaydırılmasını sağlayın.</span><span class="sxs-lookup"><span data-stu-id="05bf9-124">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="05bf9-125">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="05bf9-125">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="05bf9-126">Bu anahtar kasası bir şablon dağıtımında başvuruluyorsa, Azure Resource Manager 'ın bu anahtar kasasından gizli kod almasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="05bf9-126">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="05bf9-127">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="05bf9-127">-EnableSoftDelete</span></span>
<span data-ttu-id="05bf9-128">Bu anahtar kasası için yazılımla silme işlevinin etkinleştirildiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="05bf9-128">Specifies that the soft-delete functionality is enabled for this key vault.</span></span> <span data-ttu-id="05bf9-129">Yazılımdan silme etkinleştirildiğinde, bir yetkisiz kullanım süresi için bu anahtar kasası ve içeriğini silindikten sonra kurtarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="05bf9-129">When soft-delete is enabled, for a grace period, you can recover this key vault and its contents after it is deleted.</span></span>

<span data-ttu-id="05bf9-130">Bu işlev hakkında daha fazla bilgi [için bkz.](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete)</span><span class="sxs-lookup"><span data-stu-id="05bf9-130">For more information about this functionality, see [Azure Key Vault soft-delete overview](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span></span> <span data-ttu-id="05bf9-131">Nasıl yapılır yönergeleri için [PowerShell Ile Anahtar Kasası kolay silme 'yi kullanma](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell)konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="05bf9-131">For how-to instructions, see [How to use Key Vault soft-delete with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span></span>

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

### <span data-ttu-id="05bf9-132">-Konum</span><span class="sxs-lookup"><span data-stu-id="05bf9-132">-Location</span></span>
<span data-ttu-id="05bf9-133">Anahtar Kasası oluşturacağınız Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="05bf9-133">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="05bf9-134">Seçimlerinizi görmek için [Get-AzureLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzureLocation) komutunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="05bf9-134">Use the command [Get-AzureLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzureLocation) to see your choices.</span></span>

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

### <span data-ttu-id="05bf9-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05bf9-135">-ResourceGroupName</span></span>
<span data-ttu-id="05bf9-136">Anahtar Kasası oluşturulacak varolan bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="05bf9-136">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="05bf9-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="05bf9-137">-Sku</span></span>
<span data-ttu-id="05bf9-138">Anahtar Kasası örneğinin SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="05bf9-138">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="05bf9-139">Her SKU için hangi özelliklerin kullanılabildiği hakkında bilgi için, Azure Anahtar Kasası fiyatlandırma web sitesine ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="05bf9-139">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

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

### <span data-ttu-id="05bf9-140">Etiketli</span><span class="sxs-lookup"><span data-stu-id="05bf9-140">-Tag</span></span>
<span data-ttu-id="05bf9-141">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="05bf9-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="05bf9-142">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="05bf9-142">For example:</span></span>

<span data-ttu-id="05bf9-143">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="05bf9-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="05bf9-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="05bf9-144">-VaultName</span></span>
<span data-ttu-id="05bf9-145">Oluşturulacak Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="05bf9-145">Specifies the name of the key vault to create.</span></span> <span data-ttu-id="05bf9-146">Ad, harf, sayı veya kısa çizgi bileşimleri olabilir.</span><span class="sxs-lookup"><span data-stu-id="05bf9-146">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="05bf9-147">Ad bir harfle veya rakamla başlamalıdır ve bitmelidir.</span><span class="sxs-lookup"><span data-stu-id="05bf9-147">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="05bf9-148">Ad, evrensel olarak benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="05bf9-148">The name must be universally unique.</span></span>

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

### <span data-ttu-id="05bf9-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="05bf9-149">-Confirm</span></span>
<span data-ttu-id="05bf9-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="05bf9-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05bf9-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05bf9-151">-WhatIf</span></span>
<span data-ttu-id="05bf9-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="05bf9-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05bf9-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="05bf9-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05bf9-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05bf9-154">CommonParameters</span></span>
<span data-ttu-id="05bf9-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="05bf9-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05bf9-156">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05bf9-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05bf9-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="05bf9-157">INPUTS</span></span>

## <span data-ttu-id="05bf9-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="05bf9-158">OUTPUTS</span></span>

### <span data-ttu-id="05bf9-159">Microsoft. Azure. Commands. Keykasa. modeller. Pskasa</span><span class="sxs-lookup"><span data-stu-id="05bf9-159">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="05bf9-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="05bf9-160">NOTES</span></span>

## <span data-ttu-id="05bf9-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="05bf9-161">RELATED LINKS</span></span>

[<span data-ttu-id="05bf9-162">Get-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="05bf9-162">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="05bf9-163">Remove-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="05bf9-163">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
