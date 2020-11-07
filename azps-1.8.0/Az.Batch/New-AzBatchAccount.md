---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
ms.openlocfilehash: e996e02c9609e259c0833cfe179f295206684351
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761864"
---
# <span data-ttu-id="9e5c0-101">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="9e5c0-101">New-AzBatchAccount</span></span>

## <span data-ttu-id="9e5c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e5c0-102">SYNOPSIS</span></span>
<span data-ttu-id="9e5c0-103">Toplu hesap oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9e5c0-103">Creates a Batch account.</span></span>

## <span data-ttu-id="9e5c0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e5c0-104">SYNTAX</span></span>

```
New-AzBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-PoolAllocationMode <PoolAllocationMode>] [-KeyVaultId <String>]
 [-KeyVaultUrl <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e5c0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e5c0-105">DESCRIPTION</span></span>
<span data-ttu-id="9e5c0-106">**New-AzBatchAccount** cmdlet 'i belirtilen kaynak grubu ve konum Için bir Azure toplu hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9e5c0-106">The **New-AzBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="9e5c0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e5c0-107">EXAMPLES</span></span>

### <span data-ttu-id="9e5c0-108">Örnek 1: toplu Iş hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="9e5c0-108">Example 1: Create a Batch account</span></span>
```
PS C:\>New-AzBatchAccount -AccountName "pfuller" -ResourceGroupName "ResourceGroup03" -Location "WestUS"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : ResourceGroup03
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="9e5c0-109">Bu komut, Batı 'daki ResourceGroup03 kaynak grubunu kullanarak pfuller adlı bir toplu hesap oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9e5c0-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="9e5c0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e5c0-110">PARAMETERS</span></span>

### <span data-ttu-id="9e5c0-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9e5c0-111">-AccountName</span></span>
<span data-ttu-id="9e5c0-112">Bu cmdlet 'in oluşturduğu toplu Iş hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e5c0-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>
<span data-ttu-id="9e5c0-113">Toplu hesap adları 3 ila 24 karakter uzunluğunda olmalıdır ve yalnızca sayılar ve küçük harfler içermelidir.</span><span class="sxs-lookup"><span data-stu-id="9e5c0-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e5c0-114">-Autostorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="9e5c0-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="9e5c0-115">Otomatik depolama için kullanılacak depolama hesabının kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e5c0-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e5c0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e5c0-116">-DefaultProfile</span></span>
<span data-ttu-id="9e5c0-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9e5c0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e5c0-118">-Anahtarlı</span><span class="sxs-lookup"><span data-stu-id="9e5c0-118">-KeyVaultId</span></span>
<span data-ttu-id="9e5c0-119">Toplu hesap ile ilişkili Azure Anahtar Kasası 'nın kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="9e5c0-119">The resource ID of the Azure key vault associated with the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e5c0-120">-KeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="9e5c0-120">-KeyVaultUrl</span></span>
<span data-ttu-id="9e5c0-121">Toplu hesap ile ilişkili Azure Anahtar Kasası URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="9e5c0-121">The URL of the Azure key vault associated with the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e5c0-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="9e5c0-122">-Location</span></span>
<span data-ttu-id="9e5c0-123">Bu cmdlet 'in hesabı oluşturduğu bölgeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e5c0-123">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="9e5c0-124">Daha fazla bilgi için bkz [.](https://azure.microsoft.com/en-us/regions)</span><span class="sxs-lookup"><span data-stu-id="9e5c0-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

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

### <span data-ttu-id="9e5c0-125">-PoolAllocationMode</span><span class="sxs-lookup"><span data-stu-id="9e5c0-125">-PoolAllocationMode</span></span>
<span data-ttu-id="9e5c0-126">Toplu Iş hesabındaki havuzlar oluşturmaya yönelik ayırma modu.</span><span class="sxs-lookup"><span data-stu-id="9e5c0-126">The allocation mode for creating pools in the Batch account.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode]
Parameter Sets: (All)
Aliases:
Accepted values: BatchService, UserSubscription

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e5c0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e5c0-127">-ResourceGroupName</span></span>
<span data-ttu-id="9e5c0-128">Bu cmdlet 'in hesabı oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e5c0-128">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

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

### <span data-ttu-id="9e5c0-129">Etiketli</span><span class="sxs-lookup"><span data-stu-id="9e5c0-129">-Tag</span></span>
<span data-ttu-id="9e5c0-130">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="9e5c0-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9e5c0-131">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="9e5c0-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9e5c0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e5c0-132">CommonParameters</span></span>
<span data-ttu-id="9e5c0-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e5c0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e5c0-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e5c0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e5c0-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e5c0-135">INPUTS</span></span>

### <span data-ttu-id="9e5c0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9e5c0-136">System.String</span></span>

### <span data-ttu-id="9e5c0-137">System. Nullable ' 1 [[Microsoft.Azure.Management.Batch. Modeller. PoolAllocationMode, Microsoft.Azure.Management.Batch, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="9e5c0-137">System.Nullable\`1[[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode, Microsoft.Azure.Management.Batch, Version=4.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="9e5c0-138">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9e5c0-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9e5c0-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e5c0-139">OUTPUTS</span></span>

### <span data-ttu-id="9e5c0-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9e5c0-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9e5c0-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e5c0-141">NOTES</span></span>

## <span data-ttu-id="9e5c0-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e5c0-142">RELATED LINKS</span></span>

[<span data-ttu-id="9e5c0-143">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="9e5c0-143">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="9e5c0-144">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="9e5c0-144">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="9e5c0-145">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="9e5c0-145">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="9e5c0-146">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="9e5c0-146">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)