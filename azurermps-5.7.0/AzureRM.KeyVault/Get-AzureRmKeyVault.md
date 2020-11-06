---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
ms.openlocfilehash: 7b26eeb94854d21791bb662b4c1d9ce19973a193
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594953"
---
# <span data-ttu-id="d04a1-101">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="d04a1-101">Get-AzureRmKeyVault</span></span>

## <span data-ttu-id="d04a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d04a1-102">SYNOPSIS</span></span>
<span data-ttu-id="d04a1-103">Tuş</span><span class="sxs-lookup"><span data-stu-id="d04a1-103">Gets key vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d04a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d04a1-104">SYNTAX</span></span>

### <span data-ttu-id="d04a1-105">Listallvaultsınsubscription (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d04a1-105">ListAllVaultsInSubscription (Default)</span></span>
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d04a1-106">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="d04a1-106">GetVaultByName</span></span>
```
Get-AzureRmKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d04a1-107">Bydeletedkasası</span><span class="sxs-lookup"><span data-stu-id="d04a1-107">ByDeletedVault</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d04a1-108">Listalldeletedvaultsınsubscription</span><span class="sxs-lookup"><span data-stu-id="d04a1-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d04a1-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="d04a1-109">DESCRIPTION</span></span>
<span data-ttu-id="d04a1-110">**Get-Azurermkeykasa** cmdlet 'i, bir abonelikteki Anahtar Kasası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d04a1-110">The **Get-AzureRmKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="d04a1-111">Bir abonelikteki tüm önemli kasa örneklerini görüntüleyebilir ya da sonuçlarınızı bir kaynak grubuna veya belirli bir anahtar kasaya göre filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d04a1-111">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>

<span data-ttu-id="d04a1-112">Tek bir Anahtar Kasası aldığınızda bu cmdlet için kaynak grubu 'nun isteğe bağlı olduğunu belirten unutmayın, daha iyi performans için bunu yapmalısınız.</span><span class="sxs-lookup"><span data-stu-id="d04a1-112">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="d04a1-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d04a1-113">EXAMPLES</span></span>

### <span data-ttu-id="d04a1-114">Örnek 1: geçerli aboneliğinizdeki tüm tuş örneklerini alın</span><span class="sxs-lookup"><span data-stu-id="d04a1-114">Example 1: Get all key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRMKeyVault
```

<span data-ttu-id="d04a1-115">Bu komut geçerli aboneliğinizdeki tüm anahtarı getirir.</span><span class="sxs-lookup"><span data-stu-id="d04a1-115">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="d04a1-116">Örnek 2: belirli bir Anahtar Kasası alma</span><span class="sxs-lookup"><span data-stu-id="d04a1-116">Example 2: Get a specific key vault</span></span>
```
PS C:\>$MyVault = Get-AzureRMKeyVault -VaultName 'Contoso03Vault'
```

<span data-ttu-id="d04a1-117">Bu komut geçerli aboneliğinizde Contoso03Vault adındaki Anahtar Kasası 'nı alır ve $MyVault değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d04a1-117">This command gets the key vault named Contoso03Vault in your current subscription, and then stores it in the $MyVault variable.</span></span> <span data-ttu-id="d04a1-118">Anahtar Kasası hakkındaki ayrıntıları almak için $MyVault özelliklerini inceleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d04a1-118">You can inspect the properties of $MyVault to get details about the key vault.</span></span>

### <span data-ttu-id="d04a1-119">Örnek 3: kaynak grubundaki tuş örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="d04a1-119">Example 3: Get key vaults in a resource group</span></span>
```
PS C:\>Get-AzureRmKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

<span data-ttu-id="d04a1-120">Bu komut, ContosoPayRollResourceGroup adlı kaynak grubundaki tüm anahtarı getirir.</span><span class="sxs-lookup"><span data-stu-id="d04a1-120">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="d04a1-121">Örnek 4: geçerli aboneliğinizde tüm silinmiş anahtar örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="d04a1-121">Example 4: Get all deleted key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRmKeyVault -InRemovedState
```

<span data-ttu-id="d04a1-122">Bu komut geçerli aboneliğinizde tüm silinmiş anahtar yerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="d04a1-122">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="d04a1-123">Örnek 5: silinen bir Anahtar Kasası alma</span><span class="sxs-lookup"><span data-stu-id="d04a1-123">Example 5: Get a deleted key vault</span></span>
```
PS C:\>Get-AzureRMKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

<span data-ttu-id="d04a1-124">Bu komut, geçerli aboneliğinizde ve eastus2 bölgesinde Contoso03Vault adlı silinmiş Anahtar Kasası bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="d04a1-124">This command gets the deleted key vault information named Contoso03Vault in your current subscription and in eastus2 region.</span></span>

## <span data-ttu-id="d04a1-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d04a1-125">PARAMETERS</span></span>

### <span data-ttu-id="d04a1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d04a1-126">-DefaultProfile</span></span>
<span data-ttu-id="d04a1-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d04a1-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d04a1-128">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="d04a1-128">-InRemovedState</span></span>
<span data-ttu-id="d04a1-129">Çıktıda önceden silinmiş olan kasa gösterilip gösterilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d04a1-129">Specifies whether to show the previously deleted vaults in the output.</span></span>

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

### <span data-ttu-id="d04a1-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="d04a1-130">-Location</span></span>
<span data-ttu-id="d04a1-131">Silinmiş kasanın konumu.</span><span class="sxs-lookup"><span data-stu-id="d04a1-131">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d04a1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d04a1-132">-ResourceGroupName</span></span>
<span data-ttu-id="d04a1-133">Sorgulanan Anahtar Kasası veya anahtar kasası ile ilişkili kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d04a1-133">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

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

### <span data-ttu-id="d04a1-134">Etiketli</span><span class="sxs-lookup"><span data-stu-id="d04a1-134">-Tag</span></span>
<span data-ttu-id="d04a1-135">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="d04a1-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d04a1-136">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="d04a1-136">For example:</span></span>

<span data-ttu-id="d04a1-137">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="d04a1-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d04a1-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d04a1-138">-VaultName</span></span>
<span data-ttu-id="d04a1-139">Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d04a1-139">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d04a1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d04a1-140">CommonParameters</span></span>
<span data-ttu-id="d04a1-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d04a1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d04a1-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d04a1-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d04a1-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d04a1-143">INPUTS</span></span>

### <span data-ttu-id="d04a1-144">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d04a1-144">None</span></span>
<span data-ttu-id="d04a1-145">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="d04a1-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d04a1-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d04a1-146">OUTPUTS</span></span>

### <span data-ttu-id="d04a1-147">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="d04a1-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="d04a1-148">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultidentityıtem]</span><span class="sxs-lookup"><span data-stu-id="d04a1-148">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem]</span></span>

### <span data-ttu-id="d04a1-149">Microsoft.Azure.Commands.KeyVault.Models.PSDEleditedtuş Kasası</span><span class="sxs-lookup"><span data-stu-id="d04a1-149">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

### <span data-ttu-id="d04a1-150">System. topluluklar. Generic. LIST ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDEletedkeykasa]</span><span class="sxs-lookup"><span data-stu-id="d04a1-150">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault]</span></span>

## <span data-ttu-id="d04a1-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d04a1-151">NOTES</span></span>

## <span data-ttu-id="d04a1-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d04a1-152">RELATED LINKS</span></span>

[<span data-ttu-id="d04a1-153">Yeni-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="d04a1-153">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="d04a1-154">Remove-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="d04a1-154">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
