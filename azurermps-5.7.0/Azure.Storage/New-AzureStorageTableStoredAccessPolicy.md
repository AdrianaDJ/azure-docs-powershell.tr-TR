---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 163c6ba0841b19edc76421259b1cd9cc8411e35e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590556"
---
# <span data-ttu-id="6a14d-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6a14d-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="6a14d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a14d-102">SYNOPSIS</span></span>
<span data-ttu-id="6a14d-103">Azure depolama tablosu için depolanan bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6a14d-103">Creates a stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a14d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6a14d-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="6a14d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6a14d-105">DESCRIPTION</span></span>
<span data-ttu-id="6a14d-106">**New-AzureStorageTableStoredAccessPolicy** cmdlet 'ı bir Azure depolama tablosu için depolanan bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6a14d-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="6a14d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6a14d-107">EXAMPLES</span></span>

### <span data-ttu-id="6a14d-108">Örnek 1: tabloda depolanan bir Access ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="6a14d-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="6a14d-109">Bu komut, MyTable adlı depolama tablosunda Policy02 adlı bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6a14d-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="6a14d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6a14d-110">PARAMETERS</span></span>

### <span data-ttu-id="6a14d-111">-Context</span><span class="sxs-lookup"><span data-stu-id="6a14d-111">-Context</span></span>
<span data-ttu-id="6a14d-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a14d-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6a14d-113">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6a14d-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a14d-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6a14d-114">-ExpiryTime</span></span>
<span data-ttu-id="6a14d-115">Depolanan erişim ilkesinin geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a14d-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a14d-116">-İzin</span><span class="sxs-lookup"><span data-stu-id="6a14d-116">-Permission</span></span>
<span data-ttu-id="6a14d-117">Depolanan erişim ilkesinde depolama tablosuna erişim izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a14d-117">Specifies permissions in the stored access policy to access the storage table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a14d-118">-İlke</span><span class="sxs-lookup"><span data-stu-id="6a14d-118">-Policy</span></span>
<span data-ttu-id="6a14d-119">Depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a14d-119">Specifies a name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a14d-120">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="6a14d-120">-StartTime</span></span>
<span data-ttu-id="6a14d-121">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a14d-121">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a14d-122">-Tablo</span><span class="sxs-lookup"><span data-stu-id="6a14d-122">-Table</span></span>
<span data-ttu-id="6a14d-123">Azure depolama tablosu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a14d-123">Specifies the Azure storage table name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a14d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a14d-124">CommonParameters</span></span>
<span data-ttu-id="6a14d-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6a14d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a14d-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a14d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a14d-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6a14d-127">INPUTS</span></span>

### <span data-ttu-id="6a14d-128">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="6a14d-128">IStorageContext</span></span>

<span data-ttu-id="6a14d-129">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6a14d-129">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="6a14d-130">Dizisi</span><span class="sxs-lookup"><span data-stu-id="6a14d-130">String</span></span>

<span data-ttu-id="6a14d-131">Parametre ' tablosu ', ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6a14d-131">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="6a14d-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6a14d-132">OUTPUTS</span></span>

### <span data-ttu-id="6a14d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="6a14d-133">System.String</span></span>

## <span data-ttu-id="6a14d-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6a14d-134">NOTES</span></span>

## <span data-ttu-id="6a14d-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6a14d-135">RELATED LINKS</span></span>

[<span data-ttu-id="6a14d-136">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6a14d-136">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="6a14d-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="6a14d-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="6a14d-138">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6a14d-138">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="6a14d-139">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6a14d-139">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


