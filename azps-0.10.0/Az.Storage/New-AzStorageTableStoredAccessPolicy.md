---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 083114668fe46da6fb2ca8ba47bc540067539532
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936208"
---
# <span data-ttu-id="2fa87-101">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2fa87-101">New-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="2fa87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fa87-102">SYNOPSIS</span></span>
<span data-ttu-id="2fa87-103">Azure depolama tablosu için depolanan bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2fa87-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="2fa87-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2fa87-104">SYNTAX</span></span>

```
New-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fa87-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2fa87-105">DESCRIPTION</span></span>
<span data-ttu-id="2fa87-106">**New-AzStorageTableStoredAccessPolicy** cmdlet 'ı bir Azure depolama tablosu için depolanan bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2fa87-106">The **New-AzStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="2fa87-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2fa87-107">EXAMPLES</span></span>

### <span data-ttu-id="2fa87-108">Örnek 1: tabloda depolanan bir Access ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="2fa87-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="2fa87-109">Bu komut, MyTable adlı depolama tablosunda Policy02 adlı bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2fa87-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="2fa87-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2fa87-110">PARAMETERS</span></span>

### <span data-ttu-id="2fa87-111">-Context</span><span class="sxs-lookup"><span data-stu-id="2fa87-111">-Context</span></span>
<span data-ttu-id="2fa87-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2fa87-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2fa87-113">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2fa87-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2fa87-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fa87-114">-DefaultProfile</span></span>
<span data-ttu-id="2fa87-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2fa87-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fa87-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="2fa87-116">-ExpiryTime</span></span>
<span data-ttu-id="2fa87-117">Depolanan erişim ilkesinin geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="2fa87-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="2fa87-118">-İzin</span><span class="sxs-lookup"><span data-stu-id="2fa87-118">-Permission</span></span>
<span data-ttu-id="2fa87-119">Depolanan erişim ilkesinde depolama tablosuna erişim izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2fa87-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="2fa87-120">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="2fa87-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="2fa87-121">-İlke</span><span class="sxs-lookup"><span data-stu-id="2fa87-121">-Policy</span></span>
<span data-ttu-id="2fa87-122">Depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2fa87-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="2fa87-123">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="2fa87-123">-StartTime</span></span>
<span data-ttu-id="2fa87-124">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="2fa87-124">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="2fa87-125">-Tablo</span><span class="sxs-lookup"><span data-stu-id="2fa87-125">-Table</span></span>
<span data-ttu-id="2fa87-126">Azure depolama tablosu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2fa87-126">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="2fa87-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fa87-127">CommonParameters</span></span>
<span data-ttu-id="2fa87-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2fa87-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fa87-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fa87-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fa87-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2fa87-130">INPUTS</span></span>

### <span data-ttu-id="2fa87-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2fa87-131">System.String</span></span>

### <span data-ttu-id="2fa87-132">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="2fa87-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2fa87-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2fa87-133">OUTPUTS</span></span>

### <span data-ttu-id="2fa87-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2fa87-134">System.String</span></span>

## <span data-ttu-id="2fa87-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2fa87-135">NOTES</span></span>

## <span data-ttu-id="2fa87-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2fa87-136">RELATED LINKS</span></span>

[<span data-ttu-id="2fa87-137">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2fa87-137">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="2fa87-138">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2fa87-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="2fa87-139">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2fa87-139">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="2fa87-140">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2fa87-140">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)

