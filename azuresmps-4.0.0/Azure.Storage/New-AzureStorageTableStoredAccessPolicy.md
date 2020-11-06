---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54b28caaf39bd3d4750e341da4f4564d60b59138
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571370"
---
# <span data-ttu-id="a2eb8-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a2eb8-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="a2eb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2eb8-102">SYNOPSIS</span></span>
<span data-ttu-id="a2eb8-103">Azure depolama tablosu için depolanan bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a2eb8-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="a2eb8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a2eb8-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="a2eb8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a2eb8-105">DESCRIPTION</span></span>
<span data-ttu-id="a2eb8-106">**New-AzureStorageTableStoredAccessPolicy** cmdlet 'ı bir Azure depolama tablosu için depolanan bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a2eb8-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="a2eb8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a2eb8-107">EXAMPLES</span></span>

### <span data-ttu-id="a2eb8-108">Örnek 1: tabloda depolanan bir Access ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="a2eb8-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="a2eb8-109">Bu komut, MyTable adlı depolama tablosunda Policy02 adlı bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a2eb8-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="a2eb8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a2eb8-110">PARAMETERS</span></span>

### <span data-ttu-id="a2eb8-111">-Context</span><span class="sxs-lookup"><span data-stu-id="a2eb8-111">-Context</span></span>
<span data-ttu-id="a2eb8-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2eb8-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a2eb8-113">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a2eb8-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a2eb8-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a2eb8-114">-ExpiryTime</span></span>
<span data-ttu-id="a2eb8-115">Depolanan erişim ilkesinin geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2eb8-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="a2eb8-116">-İzin</span><span class="sxs-lookup"><span data-stu-id="a2eb8-116">-Permission</span></span>
<span data-ttu-id="a2eb8-117">Bu depolama tablosuna genel erişim düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2eb8-117">Specifies the level of public access to this storage table.</span></span>

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

### <span data-ttu-id="a2eb8-118">-İlke</span><span class="sxs-lookup"><span data-stu-id="a2eb8-118">-Policy</span></span>
<span data-ttu-id="a2eb8-119">Bu paylaşılan erişim Imzası (SAS) belirtecinin izinlerini içeren depolanan bir erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2eb8-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="a2eb8-120">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="a2eb8-120">-StartTime</span></span>
<span data-ttu-id="a2eb8-121">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2eb8-121">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="a2eb8-122">-Tablo</span><span class="sxs-lookup"><span data-stu-id="a2eb8-122">-Table</span></span>
<span data-ttu-id="a2eb8-123">Azure depolama tablosu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2eb8-123">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="a2eb8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2eb8-124">CommonParameters</span></span>
<span data-ttu-id="a2eb8-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a2eb8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2eb8-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2eb8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2eb8-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a2eb8-127">INPUTS</span></span>

## <span data-ttu-id="a2eb8-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a2eb8-128">OUTPUTS</span></span>

## <span data-ttu-id="a2eb8-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a2eb8-129">NOTES</span></span>

## <span data-ttu-id="a2eb8-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a2eb8-130">RELATED LINKS</span></span>

[<span data-ttu-id="a2eb8-131">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a2eb8-131">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="a2eb8-132">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a2eb8-132">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="a2eb8-133">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a2eb8-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="a2eb8-134">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a2eb8-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


