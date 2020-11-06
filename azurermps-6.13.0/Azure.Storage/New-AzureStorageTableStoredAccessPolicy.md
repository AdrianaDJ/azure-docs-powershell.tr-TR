---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 5a2890f052e57c37ca86197b2fd3841ba3b5c388
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593348"
---
# <span data-ttu-id="43484-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="43484-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="43484-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43484-102">SYNOPSIS</span></span>
<span data-ttu-id="43484-103">Azure depolama tablosu için depolanan bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="43484-103">Creates a stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43484-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="43484-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43484-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="43484-105">DESCRIPTION</span></span>
<span data-ttu-id="43484-106">**New-AzureStorageTableStoredAccessPolicy** cmdlet 'ı bir Azure depolama tablosu için depolanan bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="43484-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="43484-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="43484-107">EXAMPLES</span></span>

### <span data-ttu-id="43484-108">Örnek 1: tabloda depolanan bir Access ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="43484-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="43484-109">Bu komut, MyTable adlı depolama tablosunda Policy02 adlı bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="43484-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="43484-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="43484-110">PARAMETERS</span></span>

### <span data-ttu-id="43484-111">-Context</span><span class="sxs-lookup"><span data-stu-id="43484-111">-Context</span></span>
<span data-ttu-id="43484-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43484-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="43484-113">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="43484-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43484-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43484-114">-DefaultProfile</span></span>
<span data-ttu-id="43484-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="43484-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43484-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="43484-116">-ExpiryTime</span></span>
<span data-ttu-id="43484-117">Depolanan erişim ilkesinin geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="43484-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43484-118">-İzin</span><span class="sxs-lookup"><span data-stu-id="43484-118">-Permission</span></span>
<span data-ttu-id="43484-119">Depolanan erişim ilkesinde depolama tablosuna erişim izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="43484-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="43484-120">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="43484-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43484-121">-İlke</span><span class="sxs-lookup"><span data-stu-id="43484-121">-Policy</span></span>
<span data-ttu-id="43484-122">Depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43484-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="43484-123">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="43484-123">-StartTime</span></span>
<span data-ttu-id="43484-124">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="43484-124">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43484-125">-Tablo</span><span class="sxs-lookup"><span data-stu-id="43484-125">-Table</span></span>
<span data-ttu-id="43484-126">Azure depolama tablosu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43484-126">Specifies the Azure storage table name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43484-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43484-127">CommonParameters</span></span>
<span data-ttu-id="43484-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="43484-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43484-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43484-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43484-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="43484-130">INPUTS</span></span>

### <span data-ttu-id="43484-131">System. String</span><span class="sxs-lookup"><span data-stu-id="43484-131">System.String</span></span>

### <span data-ttu-id="43484-132">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="43484-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="43484-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="43484-133">OUTPUTS</span></span>

### <span data-ttu-id="43484-134">System. String</span><span class="sxs-lookup"><span data-stu-id="43484-134">System.String</span></span>

## <span data-ttu-id="43484-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="43484-135">NOTES</span></span>

## <span data-ttu-id="43484-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="43484-136">RELATED LINKS</span></span>

[<span data-ttu-id="43484-137">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="43484-137">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="43484-138">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="43484-138">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="43484-139">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="43484-139">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="43484-140">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="43484-140">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


