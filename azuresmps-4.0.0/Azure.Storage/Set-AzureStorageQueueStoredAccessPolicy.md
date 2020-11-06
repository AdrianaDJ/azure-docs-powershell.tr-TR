---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: ''
schema: 2.0.0
ms.openlocfilehash: b273dbec3fda421574c8866a10eda0a8098513ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572478"
---
# <span data-ttu-id="6498f-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6498f-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="6498f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6498f-102">SYNOPSIS</span></span>
<span data-ttu-id="6498f-103">Azure depolama sırası için depolanan bir erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6498f-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="6498f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6498f-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6498f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6498f-105">DESCRIPTION</span></span>
<span data-ttu-id="6498f-106">**Set-AzureStorageQueueStoredAccessPolicy** cmdlet 'i Azure depolama sırası için depolanan bir erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6498f-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="6498f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6498f-107">EXAMPLES</span></span>

### <span data-ttu-id="6498f-108">Örnek 1: kuyrukta depolanan bir erişim ilkesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="6498f-108">Example 1: Set a stored access policy in the queue</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07"
```

<span data-ttu-id="6498f-109">Bu komut MyQueue adındaki depolama sırası için Policy07 adlı bir erişim ilkesi ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6498f-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="6498f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6498f-110">PARAMETERS</span></span>

### <span data-ttu-id="6498f-111">-Context</span><span class="sxs-lookup"><span data-stu-id="6498f-111">-Context</span></span>
<span data-ttu-id="6498f-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6498f-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6498f-113">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6498f-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6498f-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6498f-114">-ExpiryTime</span></span>
<span data-ttu-id="6498f-115">Depolanan erişim ilkesinin geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="6498f-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="6498f-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6498f-116">-NoExpiryTime</span></span>
<span data-ttu-id="6498f-117">Erişim ilkesinde son kullanma tarihi olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6498f-117">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6498f-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="6498f-118">-NoStartTime</span></span>
<span data-ttu-id="6498f-119">Bu cmdlet 'in başlangıç zamanını $Null olarak ayarlamadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6498f-119">Indicates that this cmdlet sets the start time to be $Null.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6498f-120">-İzin</span><span class="sxs-lookup"><span data-stu-id="6498f-120">-Permission</span></span>
<span data-ttu-id="6498f-121">Bu depolama kuyruğuna genel erişim düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6498f-121">Specifies the level of public access to this storage queue.</span></span>

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

### <span data-ttu-id="6498f-122">-İlke</span><span class="sxs-lookup"><span data-stu-id="6498f-122">-Policy</span></span>
<span data-ttu-id="6498f-123">Bu SAS belirtecinin izinlerini içeren depolanan bir erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6498f-123">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="6498f-124">-Sıra</span><span class="sxs-lookup"><span data-stu-id="6498f-124">-Queue</span></span>
<span data-ttu-id="6498f-125">Azure depolama sırası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6498f-125">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="6498f-126">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="6498f-126">-StartTime</span></span>
<span data-ttu-id="6498f-127">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="6498f-127">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="6498f-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="6498f-128">-Confirm</span></span>
<span data-ttu-id="6498f-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6498f-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6498f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6498f-130">-WhatIf</span></span>
<span data-ttu-id="6498f-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6498f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6498f-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6498f-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6498f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6498f-133">CommonParameters</span></span>
<span data-ttu-id="6498f-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6498f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6498f-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6498f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6498f-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6498f-136">INPUTS</span></span>

## <span data-ttu-id="6498f-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6498f-137">OUTPUTS</span></span>

## <span data-ttu-id="6498f-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6498f-138">NOTES</span></span>

## <span data-ttu-id="6498f-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6498f-139">RELATED LINKS</span></span>

[<span data-ttu-id="6498f-140">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6498f-140">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="6498f-141">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6498f-141">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="6498f-142">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6498f-142">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)
