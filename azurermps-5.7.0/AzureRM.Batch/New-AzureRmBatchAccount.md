---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
ms.openlocfilehash: c4a8eb0bc75660c13ce8f8492b72cce8a77280e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589902"
---
# <span data-ttu-id="5b554-101">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="5b554-101">New-AzureRmBatchAccount</span></span>

## <span data-ttu-id="5b554-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b554-102">SYNOPSIS</span></span>
<span data-ttu-id="5b554-103">Toplu hesap oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5b554-103">Creates a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b554-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5b554-104">SYNTAX</span></span>

```
New-AzureRmBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-PoolAllocationMode <PoolAllocationMode>] [-KeyVaultId <String>]
 [-KeyVaultUrl <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b554-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5b554-105">DESCRIPTION</span></span>
<span data-ttu-id="5b554-106">**Yeni-AzureRmBatchAccount** cmdlet 'i belirtilen kaynak grubu ve konum Için bir Azure toplu hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5b554-106">The **New-AzureRmBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="5b554-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5b554-107">EXAMPLES</span></span>

### <span data-ttu-id="5b554-108">Örnek 1: toplu Iş hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="5b554-108">Example 1: Create a Batch account</span></span>
```
PS C:\>New-AzureRmBatchAccount -AccountName "pfuller" -ResourceGroupName "ResourceGroup03" -Location "WestUS"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : ResourceGroup03
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="5b554-109">Bu komut, Batı 'daki ResourceGroup03 kaynak grubunu kullanarak pfuller adlı bir toplu hesap oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5b554-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="5b554-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5b554-110">PARAMETERS</span></span>

### <span data-ttu-id="5b554-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5b554-111">-AccountName</span></span>
<span data-ttu-id="5b554-112">Bu cmdlet 'in oluşturduğu toplu Iş hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b554-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>

<span data-ttu-id="5b554-113">Toplu hesap adları 3 ila 24 karakter uzunluğunda olmalıdır ve yalnızca sayılar ve küçük harfler içermelidir.</span><span class="sxs-lookup"><span data-stu-id="5b554-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b554-114">-Autostorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="5b554-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="5b554-115">Otomatik depolama için kullanılacak depolama hesabının kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b554-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b554-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b554-116">-DefaultProfile</span></span>
<span data-ttu-id="5b554-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5b554-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b554-118">-Anahtarlı</span><span class="sxs-lookup"><span data-stu-id="5b554-118">-KeyVaultId</span></span>
<span data-ttu-id="5b554-119">Toplu hesap ile ilişkili Azure Anahtar Kasası 'nın kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5b554-119">The resource ID of the Azure key vault associated with the Batch account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b554-120">-KeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="5b554-120">-KeyVaultUrl</span></span>
<span data-ttu-id="5b554-121">Toplu hesap ile ilişkili Azure Anahtar Kasası URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="5b554-121">The URL of the Azure key vault associated with the Batch account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b554-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="5b554-122">-Location</span></span>
<span data-ttu-id="5b554-123">Bu cmdlet 'in hesabı oluşturduğu bölgeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b554-123">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="5b554-124">Daha fazla bilgi için bkz [.](https://azure.microsoft.com/en-us/regions)</span><span class="sxs-lookup"><span data-stu-id="5b554-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

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

### <span data-ttu-id="5b554-125">-PoolAllocationMode</span><span class="sxs-lookup"><span data-stu-id="5b554-125">-PoolAllocationMode</span></span>
<span data-ttu-id="5b554-126">Toplu Iş hesabındaki havuzlar oluşturmaya yönelik ayırma modu.</span><span class="sxs-lookup"><span data-stu-id="5b554-126">The allocation mode for creating pools in the Batch account.</span></span>

```yaml
Type: PoolAllocationMode
Parameter Sets: (All)
Aliases: 
Accepted values: BatchService, UserSubscription

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b554-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b554-127">-ResourceGroupName</span></span>
<span data-ttu-id="5b554-128">Bu cmdlet 'in hesabı oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b554-128">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

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

### <span data-ttu-id="5b554-129">Etiketli</span><span class="sxs-lookup"><span data-stu-id="5b554-129">-Tag</span></span>
<span data-ttu-id="5b554-130">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="5b554-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5b554-131">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="5b554-131">For example:</span></span>

<span data-ttu-id="5b554-132">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="5b554-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5b554-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b554-133">CommonParameters</span></span>
<span data-ttu-id="5b554-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5b554-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b554-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b554-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b554-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5b554-136">INPUTS</span></span>

### <span data-ttu-id="5b554-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5b554-137">None</span></span>
<span data-ttu-id="5b554-138">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="5b554-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5b554-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5b554-139">OUTPUTS</span></span>

### <span data-ttu-id="5b554-140">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5b554-140">BatchAccountContext</span></span>

## <span data-ttu-id="5b554-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5b554-141">NOTES</span></span>

## <span data-ttu-id="5b554-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5b554-142">RELATED LINKS</span></span>

[<span data-ttu-id="5b554-143">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="5b554-143">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="5b554-144">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="5b554-144">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="5b554-145">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="5b554-145">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="5b554-146">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="5b554-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
