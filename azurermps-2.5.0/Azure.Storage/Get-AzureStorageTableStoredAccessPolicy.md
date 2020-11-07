---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragetablestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: a9c141684eb924ed0b969c469214d92b847e13db
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939644"
---
# <span data-ttu-id="04f64-101">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="04f64-101">Get-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="04f64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04f64-102">SYNOPSIS</span></span>
<span data-ttu-id="04f64-103">Azure depolama tablosu için depolanan erişim ilkesini veya ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="04f64-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04f64-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="04f64-104">SYNTAX</span></span>

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04f64-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="04f64-105">DESCRIPTION</span></span>
<span data-ttu-id="04f64-106">**Get-AzureStorageTableStoredAccessPolicy** cmdlet 'i, bir Azure depolama tablosu için depolanan erişim ilkesini veya ilkelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="04f64-106">The **Get-AzureStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="04f64-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="04f64-107">EXAMPLES</span></span>

### <span data-ttu-id="04f64-108">Örnek 1: depolama tablosunda depolanan bir erişim ilkesi alma</span><span class="sxs-lookup"><span data-stu-id="04f64-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="04f64-109">Bu komut, Table02 adındaki depolama tablosundaki Policy50 adındaki erişim ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="04f64-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="04f64-110">Örnek 2: depolama tablosunda tüm depolanan erişim ilkelerini alma</span><span class="sxs-lookup"><span data-stu-id="04f64-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="04f64-111">Bu komut, Table02 adlı tablodaki tüm erişim ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="04f64-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="04f64-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="04f64-112">PARAMETERS</span></span>

### <span data-ttu-id="04f64-113">-Context</span><span class="sxs-lookup"><span data-stu-id="04f64-113">-Context</span></span>
<span data-ttu-id="04f64-114">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="04f64-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="04f64-115">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="04f64-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="04f64-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04f64-116">-DefaultProfile</span></span>
<span data-ttu-id="04f64-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="04f64-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04f64-118">-İlke</span><span class="sxs-lookup"><span data-stu-id="04f64-118">-Policy</span></span>
<span data-ttu-id="04f64-119">Bu paylaşılan erişim Imzası (SAS) belirtecinin izinlerini içeren depolanan bir erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="04f64-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04f64-120">-Tablo</span><span class="sxs-lookup"><span data-stu-id="04f64-120">-Table</span></span>
<span data-ttu-id="04f64-121">Azure depolama tablosu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="04f64-121">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="04f64-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04f64-122">CommonParameters</span></span>
<span data-ttu-id="04f64-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="04f64-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04f64-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04f64-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04f64-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="04f64-125">INPUTS</span></span>

### <span data-ttu-id="04f64-126">System. String</span><span class="sxs-lookup"><span data-stu-id="04f64-126">System.String</span></span>

### <span data-ttu-id="04f64-127">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="04f64-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="04f64-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="04f64-128">OUTPUTS</span></span>

### <span data-ttu-id="04f64-129">Microsoft. Windowsazde. Storage. Table. SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="04f64-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="04f64-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="04f64-130">NOTES</span></span>

## <span data-ttu-id="04f64-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="04f64-131">RELATED LINKS</span></span>

[<span data-ttu-id="04f64-132">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="04f64-132">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="04f64-133">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="04f64-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="04f64-134">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="04f64-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="04f64-135">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="04f64-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


