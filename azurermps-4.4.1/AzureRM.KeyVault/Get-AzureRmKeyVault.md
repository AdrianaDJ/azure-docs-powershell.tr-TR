---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://go.microsoft.com/fwlink/?LinkID=690161
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
ms.openlocfilehash: 9a4d3399dd19d7dfced4f695623eef2fe0dba29d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587917"
---
# <span data-ttu-id="f9562-101">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="f9562-101">Get-AzureRmKeyVault</span></span>

## <span data-ttu-id="f9562-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9562-102">SYNOPSIS</span></span>
<span data-ttu-id="f9562-103">Tuş</span><span class="sxs-lookup"><span data-stu-id="f9562-103">Gets key vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9562-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f9562-104">SYNTAX</span></span>

### <span data-ttu-id="f9562-105">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="f9562-105">GetVaultByName</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9562-106">Bydeletedkasası</span><span class="sxs-lookup"><span data-stu-id="f9562-106">ByDeletedVault</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9562-107">ListVaultsByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f9562-107">ListVaultsByResourceGroup</span></span>
```
Get-AzureRmKeyVault [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f9562-108">Listalldeletedvaultsınsubscription</span><span class="sxs-lookup"><span data-stu-id="f9562-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9562-109">Listallvaultsınsubscription</span><span class="sxs-lookup"><span data-stu-id="f9562-109">ListAllVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9562-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="f9562-110">DESCRIPTION</span></span>
<span data-ttu-id="f9562-111">**Get-Azurermkeykasa** cmdlet 'i, bir abonelikteki Anahtar Kasası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="f9562-111">The **Get-AzureRmKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="f9562-112">Bir abonelikteki tüm önemli kasa örneklerini görüntüleyebilir ya da sonuçlarınızı bir kaynak grubuna veya belirli bir anahtar kasaya göre filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f9562-112">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>

<span data-ttu-id="f9562-113">Tek bir Anahtar Kasası aldığınızda bu cmdlet için kaynak grubu 'nun isteğe bağlı olduğunu belirten unutmayın, daha iyi performans için bunu yapmalısınız.</span><span class="sxs-lookup"><span data-stu-id="f9562-113">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="f9562-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f9562-114">EXAMPLES</span></span>

### <span data-ttu-id="f9562-115">Örnek 1: geçerli aboneliğinizdeki tüm tuş örneklerini alın</span><span class="sxs-lookup"><span data-stu-id="f9562-115">Example 1: Get all key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRMKeyVault
```

<span data-ttu-id="f9562-116">Bu komut geçerli aboneliğinizdeki tüm anahtarı getirir.</span><span class="sxs-lookup"><span data-stu-id="f9562-116">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="f9562-117">Örnek 2: belirli bir Anahtar Kasası alma</span><span class="sxs-lookup"><span data-stu-id="f9562-117">Example 2: Get a specific key vault</span></span>
```
PS C:\>$MyVault = Get-AzureRMKeyVault -VaultName 'Contoso03Vault'
```

<span data-ttu-id="f9562-118">Bu komut geçerli aboneliğinizde Contoso03Vault adındaki Anahtar Kasası 'nı alır ve $MyVault değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f9562-118">This command gets the key vault named Contoso03Vault in your current subscription, and then stores it in the $MyVault variable.</span></span> <span data-ttu-id="f9562-119">Anahtar Kasası hakkındaki ayrıntıları almak için $MyVault özelliklerini inceleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f9562-119">You can inspect the properties of $MyVault to get details about the key vault.</span></span>

### <span data-ttu-id="f9562-120">Örnek 3: kaynak grubundaki tuş örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="f9562-120">Example 3: Get key vaults in a resource group</span></span>
```
PS C:\>Get-AzureRmKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

<span data-ttu-id="f9562-121">Bu komut, ContosoPayRollResourceGroup adlı kaynak grubundaki tüm anahtarı getirir.</span><span class="sxs-lookup"><span data-stu-id="f9562-121">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="f9562-122">Örnek 4: geçerli aboneliğinizde tüm silinmiş anahtar örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="f9562-122">Example 4: Get all deleted key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRmKeyVault -InRemovedState
```

<span data-ttu-id="f9562-123">Bu komut geçerli aboneliğinizde tüm silinmiş anahtar yerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="f9562-123">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="f9562-124">Örnek 5: silinen bir Anahtar Kasası alma</span><span class="sxs-lookup"><span data-stu-id="f9562-124">Example 5: Get a deleted key vault</span></span>
```
PS C:\>Get-AzureRMKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

<span data-ttu-id="f9562-125">Bu komut, geçerli aboneliğinizde ve eastus2 bölgesinde Contoso03Vault adlı silinmiş Anahtar Kasası bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="f9562-125">This command gets the deleted key vault information named Contoso03Vault in your current subscription and in eastus2 region.</span></span>

## <span data-ttu-id="f9562-126">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f9562-126">PARAMETERS</span></span>

### <span data-ttu-id="f9562-127">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="f9562-127">-InRemovedState</span></span>
<span data-ttu-id="f9562-128">Çıktıda önceden silinmiş olan kasa gösterilip gösterilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9562-128">Specifies whether to show the previously deleted vaults in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9562-129">-Konum</span><span class="sxs-lookup"><span data-stu-id="f9562-129">-Location</span></span>
<span data-ttu-id="f9562-130">Silinmiş kasanın konumu.</span><span class="sxs-lookup"><span data-stu-id="f9562-130">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9562-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9562-131">-ResourceGroupName</span></span>
<span data-ttu-id="f9562-132">Sorgulanan Anahtar Kasası veya anahtar kasası ile ilişkili kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9562-132">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListVaultsByResourceGroup
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9562-133">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f9562-133">-Tag</span></span>
<span data-ttu-id="f9562-134">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="f9562-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f9562-135">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="f9562-135">For example:</span></span>

<span data-ttu-id="f9562-136">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="f9562-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9562-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f9562-137">-VaultName</span></span>
<span data-ttu-id="f9562-138">Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9562-138">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName, ByDeletedVault
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9562-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9562-139">-DefaultProfile</span></span>
<span data-ttu-id="f9562-140">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f9562-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9562-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9562-141">CommonParameters</span></span>
<span data-ttu-id="f9562-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f9562-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9562-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9562-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9562-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f9562-144">INPUTS</span></span>

## <span data-ttu-id="f9562-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f9562-145">OUTPUTS</span></span>

### <span data-ttu-id="f9562-146">Microsoft. Azure. Commands. Keykasa. modeller. Pskasa</span><span class="sxs-lookup"><span data-stu-id="f9562-146">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

### <span data-ttu-id="f9562-147">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Keykasa. modeller. Psvaultidentityıtem]</span><span class="sxs-lookup"><span data-stu-id="f9562-147">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSVaultIdentityItem]</span></span>

### <span data-ttu-id="f9562-148">Microsoft.Azure.Commands.KeyVault.Models.PSDon kasa</span><span class="sxs-lookup"><span data-stu-id="f9562-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span></span>

### <span data-ttu-id="f9562-149">System. topluluklar. Generic. LIST ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDEletedkasa]</span><span class="sxs-lookup"><span data-stu-id="f9562-149">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span></span>

## <span data-ttu-id="f9562-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f9562-150">NOTES</span></span>

## <span data-ttu-id="f9562-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f9562-151">RELATED LINKS</span></span>

[<span data-ttu-id="f9562-152">Yeni-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="f9562-152">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="f9562-153">Remove-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="f9562-153">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
