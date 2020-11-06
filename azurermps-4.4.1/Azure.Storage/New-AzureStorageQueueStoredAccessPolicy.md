---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: ef54976ed06eb47da803470a3d4c163a8b294743
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595054"
---
# <span data-ttu-id="acdf9-101">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="acdf9-101">New-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="acdf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acdf9-102">SYNOPSIS</span></span>
<span data-ttu-id="acdf9-103">Azure depolama sırası için depolanan bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="acdf9-103">Creates a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acdf9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="acdf9-104">SYNTAX</span></span>

```
New-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="acdf9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="acdf9-105">DESCRIPTION</span></span>
<span data-ttu-id="acdf9-106">**New-AzureStorageQueueStoredAccessPolicy** cmdlet 'i Azure depolama sırası için depolanan bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="acdf9-106">The **New-AzureStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="acdf9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="acdf9-107">EXAMPLES</span></span>

### <span data-ttu-id="acdf9-108">Örnek 1: depolama sırasında depolanan bir erişim ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="acdf9-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="acdf9-109">Bu komut MyQueue adındaki depolama sırasında Policy01 adlı bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="acdf9-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="acdf9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="acdf9-110">PARAMETERS</span></span>

### <span data-ttu-id="acdf9-111">-Context</span><span class="sxs-lookup"><span data-stu-id="acdf9-111">-Context</span></span>
<span data-ttu-id="acdf9-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="acdf9-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="acdf9-113">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="acdf9-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="acdf9-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="acdf9-114">-ExpiryTime</span></span>
<span data-ttu-id="acdf9-115">Depolanan erişim ilkesinin geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="acdf9-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="acdf9-116">-İzin</span><span class="sxs-lookup"><span data-stu-id="acdf9-116">-Permission</span></span>
<span data-ttu-id="acdf9-117">Depolanan erişim ilkesinde depolama kuyruğuna erişim izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="acdf9-117">Specifies permissions in the stored access policy to access the storage queue.</span></span>

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

### <span data-ttu-id="acdf9-118">-İlke</span><span class="sxs-lookup"><span data-stu-id="acdf9-118">-Policy</span></span>
<span data-ttu-id="acdf9-119">Depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="acdf9-119">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="acdf9-120">-Sıra</span><span class="sxs-lookup"><span data-stu-id="acdf9-120">-Queue</span></span>
<span data-ttu-id="acdf9-121">Azure depolama sırası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="acdf9-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="acdf9-122">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="acdf9-122">-StartTime</span></span>
<span data-ttu-id="acdf9-123">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="acdf9-123">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="acdf9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acdf9-124">CommonParameters</span></span>
<span data-ttu-id="acdf9-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="acdf9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acdf9-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acdf9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acdf9-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="acdf9-127">INPUTS</span></span>

### <span data-ttu-id="acdf9-128">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="acdf9-128">IStorageContext</span></span>

<span data-ttu-id="acdf9-129">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="acdf9-129">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="acdf9-130">Dizisi</span><span class="sxs-lookup"><span data-stu-id="acdf9-130">String</span></span>

<span data-ttu-id="acdf9-131">' Queue ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="acdf9-131">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="acdf9-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="acdf9-132">OUTPUTS</span></span>

### <span data-ttu-id="acdf9-133">System. String</span><span class="sxs-lookup"><span data-stu-id="acdf9-133">System.String</span></span>

## <span data-ttu-id="acdf9-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="acdf9-134">NOTES</span></span>

## <span data-ttu-id="acdf9-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="acdf9-135">RELATED LINKS</span></span>

[<span data-ttu-id="acdf9-136">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="acdf9-136">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="acdf9-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="acdf9-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="acdf9-138">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="acdf9-138">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="acdf9-139">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="acdf9-139">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)


