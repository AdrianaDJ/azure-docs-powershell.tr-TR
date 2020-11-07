---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 578eef176903576778325eb8610870040a515751
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761766"
---
# <span data-ttu-id="aeb9f-101">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aeb9f-101">New-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="aeb9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aeb9f-102">SYNOPSIS</span></span>
<span data-ttu-id="aeb9f-103">Azure depolama sırası için depolanan bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aeb9f-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="aeb9f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aeb9f-104">SYNTAX</span></span>

```
New-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="aeb9f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="aeb9f-105">DESCRIPTION</span></span>
<span data-ttu-id="aeb9f-106">**New-AzureStorageQueueStoredAccessPolicy** cmdlet 'i Azure depolama sırası için depolanan bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aeb9f-106">The **New-AzureStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="aeb9f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aeb9f-107">EXAMPLES</span></span>

### <span data-ttu-id="aeb9f-108">Örnek 1: depolama sırasında depolanan bir erişim ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="aeb9f-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="aeb9f-109">Bu komut MyQueue adındaki depolama sırasında Policy01 adlı bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aeb9f-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="aeb9f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aeb9f-110">PARAMETERS</span></span>

### <span data-ttu-id="aeb9f-111">-Context</span><span class="sxs-lookup"><span data-stu-id="aeb9f-111">-Context</span></span>
<span data-ttu-id="aeb9f-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeb9f-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="aeb9f-113">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="aeb9f-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="aeb9f-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="aeb9f-114">-ExpiryTime</span></span>
<span data-ttu-id="aeb9f-115">Depolanan erişim ilkesinin geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeb9f-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="aeb9f-116">-İzin</span><span class="sxs-lookup"><span data-stu-id="aeb9f-116">-Permission</span></span>
<span data-ttu-id="aeb9f-117">Bu depolama kuyruğuna genel erişim düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeb9f-117">Specifies the level of public access to this storage queue.</span></span>

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

### <span data-ttu-id="aeb9f-118">-İlke</span><span class="sxs-lookup"><span data-stu-id="aeb9f-118">-Policy</span></span>
<span data-ttu-id="aeb9f-119">Bu SAS belirtecinin izinlerini içeren depolanan bir erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeb9f-119">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="aeb9f-120">-Sıra</span><span class="sxs-lookup"><span data-stu-id="aeb9f-120">-Queue</span></span>
<span data-ttu-id="aeb9f-121">Azure depolama sırası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeb9f-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="aeb9f-122">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="aeb9f-122">-StartTime</span></span>
<span data-ttu-id="aeb9f-123">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeb9f-123">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="aeb9f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeb9f-124">CommonParameters</span></span>
<span data-ttu-id="aeb9f-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aeb9f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeb9f-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aeb9f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeb9f-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aeb9f-127">INPUTS</span></span>

## <span data-ttu-id="aeb9f-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aeb9f-128">OUTPUTS</span></span>

## <span data-ttu-id="aeb9f-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aeb9f-129">NOTES</span></span>

## <span data-ttu-id="aeb9f-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aeb9f-130">RELATED LINKS</span></span>

[<span data-ttu-id="aeb9f-131">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aeb9f-131">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="aeb9f-132">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="aeb9f-132">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="aeb9f-133">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aeb9f-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="aeb9f-134">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aeb9f-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)


