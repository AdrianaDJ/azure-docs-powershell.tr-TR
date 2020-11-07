---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurermkeyvault
schema: 2.0.0
ms.openlocfilehash: 7cbcf722b71919096ca2c7d1dc3201ad2fe42f2a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939725"
---
# <span data-ttu-id="209f1-101">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="209f1-101">Get-AzureRmKeyVault</span></span>

## <span data-ttu-id="209f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="209f1-102">SYNOPSIS</span></span>
<span data-ttu-id="209f1-103">Tuş</span><span class="sxs-lookup"><span data-stu-id="209f1-103">Gets key vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="209f1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="209f1-104">SYNTAX</span></span>

### <span data-ttu-id="209f1-105">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="209f1-105">GetVaultByName</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="209f1-106">Bydeletedkasası</span><span class="sxs-lookup"><span data-stu-id="209f1-106">ByDeletedVault</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="209f1-107">ListVaultsByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="209f1-107">ListVaultsByResourceGroup</span></span>
```
Get-AzureRmKeyVault [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="209f1-108">Listalldeletedvaultsınsubscription</span><span class="sxs-lookup"><span data-stu-id="209f1-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="209f1-109">Listallvaultsınsubscription</span><span class="sxs-lookup"><span data-stu-id="209f1-109">ListAllVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="209f1-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="209f1-110">DESCRIPTION</span></span>
<span data-ttu-id="209f1-111">**Get-Azurermkeykasa** cmdlet 'i, bir abonelikteki Anahtar Kasası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="209f1-111">The **Get-AzureRmKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="209f1-112">Bir abonelikteki tüm önemli kasa örneklerini görüntüleyebilir ya da sonuçlarınızı bir kaynak grubuna veya belirli bir anahtar kasaya göre filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="209f1-112">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>

<span data-ttu-id="209f1-113">Tek bir Anahtar Kasası aldığınızda bu cmdlet için kaynak grubu 'nun isteğe bağlı olduğunu belirten unutmayın, daha iyi performans için bunu yapmalısınız.</span><span class="sxs-lookup"><span data-stu-id="209f1-113">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="209f1-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="209f1-114">EXAMPLES</span></span>

### <span data-ttu-id="209f1-115">Örnek 1: geçerli aboneliğinizdeki tüm tuş örneklerini alın</span><span class="sxs-lookup"><span data-stu-id="209f1-115">Example 1: Get all key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRMKeyVault
```

<span data-ttu-id="209f1-116">Bu komut geçerli aboneliğinizdeki tüm anahtarı getirir.</span><span class="sxs-lookup"><span data-stu-id="209f1-116">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="209f1-117">Örnek 2: belirli bir Anahtar Kasası alma</span><span class="sxs-lookup"><span data-stu-id="209f1-117">Example 2: Get a specific key vault</span></span>
```
PS C:\>$MyVault = Get-AzureRMKeyVault -VaultName 'Contoso03Vault'
```

<span data-ttu-id="209f1-118">Bu komut geçerli aboneliğinizde Contoso03Vault adındaki Anahtar Kasası 'nı alır ve $MyVault değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="209f1-118">This command gets the key vault named Contoso03Vault in your current subscription, and then stores it in the $MyVault variable.</span></span> <span data-ttu-id="209f1-119">Anahtar Kasası hakkındaki ayrıntıları almak için $MyVault özelliklerini inceleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="209f1-119">You can inspect the properties of $MyVault to get details about the key vault.</span></span>

### <span data-ttu-id="209f1-120">Örnek 3: kaynak grubundaki tuş örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="209f1-120">Example 3: Get key vaults in a resource group</span></span>
```
PS C:\>Get-AzureRmKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

<span data-ttu-id="209f1-121">Bu komut, ContosoPayRollResourceGroup adlı kaynak grubundaki tüm anahtarı getirir.</span><span class="sxs-lookup"><span data-stu-id="209f1-121">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="209f1-122">Örnek 4: geçerli aboneliğinizde tüm silinmiş anahtar örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="209f1-122">Example 4: Get all deleted key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRmKeyVault -InRemovedState
```

<span data-ttu-id="209f1-123">Bu komut geçerli aboneliğinizde tüm silinmiş anahtar yerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="209f1-123">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="209f1-124">Örnek 5: silinen bir Anahtar Kasası alma</span><span class="sxs-lookup"><span data-stu-id="209f1-124">Example 5: Get a deleted key vault</span></span>
```
PS C:\>Get-AzureRMKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

<span data-ttu-id="209f1-125">Bu komut, geçerli aboneliğinizde ve eastus2 bölgesinde Contoso03Vault adlı silinmiş Anahtar Kasası bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="209f1-125">This command gets the deleted key vault information named Contoso03Vault in your current subscription and in eastus2 region.</span></span>

## <span data-ttu-id="209f1-126">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="209f1-126">PARAMETERS</span></span>

### <span data-ttu-id="209f1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="209f1-127">-DefaultProfile</span></span>
<span data-ttu-id="209f1-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="209f1-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="209f1-129">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="209f1-129">-InRemovedState</span></span>
<span data-ttu-id="209f1-130">Çıktıda önceden silinmiş olan kasa gösterilip gösterilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="209f1-130">Specifies whether to show the previously deleted vaults in the output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="209f1-131">-Konum</span><span class="sxs-lookup"><span data-stu-id="209f1-131">-Location</span></span>
<span data-ttu-id="209f1-132">Silinmiş kasanın konumu.</span><span class="sxs-lookup"><span data-stu-id="209f1-132">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="209f1-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="209f1-133">-ResourceGroupName</span></span>
<span data-ttu-id="209f1-134">Sorgulanan Anahtar Kasası veya anahtar kasası ile ilişkili kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="209f1-134">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListVaultsByResourceGroup
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="209f1-135">Etiketli</span><span class="sxs-lookup"><span data-stu-id="209f1-135">-Tag</span></span>
<span data-ttu-id="209f1-136">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="209f1-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="209f1-137">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="209f1-137">For example:</span></span>

<span data-ttu-id="209f1-138">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="209f1-138">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="209f1-139">-VaultName</span><span class="sxs-lookup"><span data-stu-id="209f1-139">-VaultName</span></span>
<span data-ttu-id="209f1-140">Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="209f1-140">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName, ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="209f1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="209f1-141">CommonParameters</span></span>
<span data-ttu-id="209f1-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="209f1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="209f1-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="209f1-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="209f1-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="209f1-144">INPUTS</span></span>

## <span data-ttu-id="209f1-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="209f1-145">OUTPUTS</span></span>

### <span data-ttu-id="209f1-146">Microsoft. Azure. Commands. Keykasa. modeller. Pskasa</span><span class="sxs-lookup"><span data-stu-id="209f1-146">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

### <span data-ttu-id="209f1-147">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Keykasa. modeller. Psvaultidentityıtem]</span><span class="sxs-lookup"><span data-stu-id="209f1-147">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSVaultIdentityItem]</span></span>

### <span data-ttu-id="209f1-148">Microsoft.Azure.Commands.KeyVault.Models.PSDon kasa</span><span class="sxs-lookup"><span data-stu-id="209f1-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span></span>

### <span data-ttu-id="209f1-149">System. topluluklar. Generic. LIST ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDEletedkasa]</span><span class="sxs-lookup"><span data-stu-id="209f1-149">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span></span>

## <span data-ttu-id="209f1-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="209f1-150">NOTES</span></span>

## <span data-ttu-id="209f1-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="209f1-151">RELATED LINKS</span></span>

[<span data-ttu-id="209f1-152">Yeni-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="209f1-152">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="209f1-153">Remove-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="209f1-153">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
