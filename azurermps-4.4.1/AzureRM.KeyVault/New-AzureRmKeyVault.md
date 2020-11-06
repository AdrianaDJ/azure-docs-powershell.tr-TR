---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://go.microsoft.com/fwlink/?LinkId=690160
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
ms.openlocfilehash: 28cd93fe9de14365e4de626729ec45a7aaa88cdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594661"
---
# <span data-ttu-id="4585f-101">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="4585f-101">New-AzureRmKeyVault</span></span>

## <span data-ttu-id="4585f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4585f-102">SYNOPSIS</span></span>
<span data-ttu-id="4585f-103">Bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4585f-103">Creates a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4585f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4585f-104">SYNTAX</span></span>

```
New-AzureRmKeyVault [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete]
 [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4585f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4585f-105">DESCRIPTION</span></span>
<span data-ttu-id="4585f-106">**Yeni-Azurermkeykasa** cmdlet 'i belirtilen kaynak grubunda bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4585f-106">The **New-AzureRmKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="4585f-107">Bu cmdlet, şu anda oturum açmış olan kullanıcıya, anahtar kasasındaki anahtarları ve gizlilikleri eklemek, kaldırmak veya listelemek amacıyla izinler verir.</span><span class="sxs-lookup"><span data-stu-id="4585f-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>

<span data-ttu-id="4585f-108">Not: Bu hata, **abonelik ' Microsoft. keykasa ' ad alanını kullanacak şekilde kaydedilmediğini** görürseniz **, yeni anahtar** kasayı oluşturmaya çalıştığınızda, **register-AzureRmResourceProvider-ProviderNamespace-Providernamespace-providerın**</span><span class="sxs-lookup"><span data-stu-id="4585f-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzureRmKeyVault** command.</span></span> <span data-ttu-id="4585f-109">Daha fazla bilgi için Register-AzureRmResourceProvider konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="4585f-109">For more information, see Register-AzureRmResourceProvider.</span></span>

## <span data-ttu-id="4585f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4585f-110">EXAMPLES</span></span>

### <span data-ttu-id="4585f-111">Örnek 1: standart bir Anahtar Kasası oluşturma</span><span class="sxs-lookup"><span data-stu-id="4585f-111">Example 1: Create a Standard key vault</span></span>
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

<span data-ttu-id="4585f-112">Bu komut, Azure bölgesinde Contoso03Vault adlı bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4585f-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="4585f-113">Komut, anahtar kasayı Group14 adlı kaynak grubuna ekler.</span><span class="sxs-lookup"><span data-stu-id="4585f-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="4585f-114">Komut, *SKU* parametresi için bir değer belirtmediğinden, standart bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4585f-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="4585f-115">Örnek 2: Premium Anahtar Kasası oluşturma</span><span class="sxs-lookup"><span data-stu-id="4585f-115">Example 2: Create a Premium key vault</span></span>
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'
```

<span data-ttu-id="4585f-116">Bu komut, önceki örnekte olduğu gibi bir Anahtar Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4585f-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="4585f-117">Bununla birlikte, Özel Anahtar Kasası oluşturmak için *SKU* parametresi için Premium değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4585f-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

## <span data-ttu-id="4585f-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4585f-118">PARAMETERS</span></span>

### <span data-ttu-id="4585f-119">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="4585f-119">-EnabledForDeployment</span></span>
<span data-ttu-id="4585f-120">Kaynak oluşturmada bu Anahtar Kasası, örneğin sanal makine oluştururken bu anahtar kasasına başvurulduğunda, Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4585f-120">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4585f-121">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="4585f-121">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="4585f-122">Azure disk şifreleme hizmeti 'nin, bu anahtar kasasından parolaları almasını ve anahtarları kaydırılmasını sağlayın.</span><span class="sxs-lookup"><span data-stu-id="4585f-122">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4585f-123">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="4585f-123">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="4585f-124">Bu anahtar kasası bir şablon dağıtımında başvuruluyorsa, Azure Resource Manager 'ın bu anahtar kasasından gizli kod almasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="4585f-124">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4585f-125">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="4585f-125">-EnableSoftDelete</span></span>
<span data-ttu-id="4585f-126">Belirtilmişse, bu Anahtar Kasası için ' yumuşak silme ' işlevi etkinleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="4585f-126">If specified, 'soft delete' functionality is enabled for this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4585f-127">-Konum</span><span class="sxs-lookup"><span data-stu-id="4585f-127">-Location</span></span>
<span data-ttu-id="4585f-128">Anahtar Kasası oluşturacağınız Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4585f-128">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="4585f-129"> https://msdn.microsoft.com/Seçimlerinizi görmek için komut Get-AzureLocation (Library/Azure/mt589064. aspx) kullanın.</span><span class="sxs-lookup"><span data-stu-id="4585f-129">Use the command Get-AzureLocation (https://msdn.microsoft.com/ library/azure/mt589064.aspx) to see your choices.</span></span> <span data-ttu-id="4585f-130">Daha fazla bilgi için yazın `Get-Help Get-AzureLocation` .</span><span class="sxs-lookup"><span data-stu-id="4585f-130">For more information, type `Get-Help Get-AzureLocation`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4585f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4585f-131">-ResourceGroupName</span></span>
<span data-ttu-id="4585f-132">Anahtar Kasası oluşturulacak varolan bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4585f-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4585f-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="4585f-133">-Sku</span></span>
<span data-ttu-id="4585f-134">Anahtar Kasası örneğinin SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4585f-134">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="4585f-135">Her SKU için hangi özelliklerin kullanılabildiği hakkında bilgi için, Azure Anahtar Kasası fiyatlandırma web sitesine ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="4585f-135">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: Microsoft.Azure.Management.KeyVault.Models.SkuName
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4585f-136">Etiketli</span><span class="sxs-lookup"><span data-stu-id="4585f-136">-Tag</span></span>
<span data-ttu-id="4585f-137">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="4585f-137">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4585f-138">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="4585f-138">For example:</span></span>

<span data-ttu-id="4585f-139">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="4585f-139">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4585f-140">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4585f-140">-VaultName</span></span>
<span data-ttu-id="4585f-141">Oluşturulacak Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4585f-141">Specifies the name of the key vault to create.</span></span> <span data-ttu-id="4585f-142">Ad, harf, sayı veya kısa çizgi bileşimleri olabilir.</span><span class="sxs-lookup"><span data-stu-id="4585f-142">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="4585f-143">Ad bir harfle veya rakamla başlamalıdır ve bitmelidir.</span><span class="sxs-lookup"><span data-stu-id="4585f-143">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="4585f-144">Ad, evrensel olarak benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4585f-144">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4585f-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="4585f-145">-Confirm</span></span>
<span data-ttu-id="4585f-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4585f-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4585f-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4585f-147">-WhatIf</span></span>
<span data-ttu-id="4585f-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4585f-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4585f-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4585f-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4585f-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4585f-150">-DefaultProfile</span></span>
<span data-ttu-id="4585f-151">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4585f-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4585f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4585f-152">CommonParameters</span></span>
<span data-ttu-id="4585f-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4585f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4585f-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4585f-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4585f-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4585f-155">INPUTS</span></span>

## <span data-ttu-id="4585f-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4585f-156">OUTPUTS</span></span>

### <span data-ttu-id="4585f-157">Microsoft. Azure. Commands. Keykasa. modeller. Pskasa</span><span class="sxs-lookup"><span data-stu-id="4585f-157">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="4585f-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4585f-158">NOTES</span></span>

## <span data-ttu-id="4585f-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4585f-159">RELATED LINKS</span></span>

[<span data-ttu-id="4585f-160">Get-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="4585f-160">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="4585f-161">Remove-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="4585f-161">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
