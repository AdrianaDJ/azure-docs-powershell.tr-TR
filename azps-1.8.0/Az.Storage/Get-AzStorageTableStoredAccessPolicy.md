---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: f66fc4a0581d41b7746322dd8fe9ffe8bb8b50e1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758640"
---
# <span data-ttu-id="b3a4f-101">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b3a4f-101">Get-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="b3a4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3a4f-102">SYNOPSIS</span></span>
<span data-ttu-id="b3a4f-103">Azure depolama tablosu için depolanan erişim ilkesini veya ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="b3a4f-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="b3a4f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3a4f-104">SYNTAX</span></span>

```
Get-AzStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3a4f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3a4f-105">DESCRIPTION</span></span>
<span data-ttu-id="b3a4f-106">**Get-AzStorageTableStoredAccessPolicy** cmdlet 'ı, Azure depolama tablosu için depolanan erişim ilkesini veya ilkelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="b3a4f-106">The **Get-AzStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="b3a4f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3a4f-107">EXAMPLES</span></span>

### <span data-ttu-id="b3a4f-108">Örnek 1: depolama tablosunda depolanan bir erişim ilkesi alma</span><span class="sxs-lookup"><span data-stu-id="b3a4f-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="b3a4f-109">Bu komut, Table02 adındaki depolama tablosundaki Policy50 adındaki erişim ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="b3a4f-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="b3a4f-110">Örnek 2: depolama tablosunda tüm depolanan erişim ilkelerini alma</span><span class="sxs-lookup"><span data-stu-id="b3a4f-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="b3a4f-111">Bu komut, Table02 adlı tablodaki tüm erişim ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="b3a4f-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="b3a4f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3a4f-112">PARAMETERS</span></span>

### <span data-ttu-id="b3a4f-113">-Context</span><span class="sxs-lookup"><span data-stu-id="b3a4f-113">-Context</span></span>
<span data-ttu-id="b3a4f-114">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3a4f-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b3a4f-115">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b3a4f-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b3a4f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3a4f-116">-DefaultProfile</span></span>
<span data-ttu-id="b3a4f-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b3a4f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3a4f-118">-İlke</span><span class="sxs-lookup"><span data-stu-id="b3a4f-118">-Policy</span></span>
<span data-ttu-id="b3a4f-119">Bu paylaşılan erişim Imzası (SAS) belirtecinin izinlerini içeren depolanan bir erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3a4f-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="b3a4f-120">-Tablo</span><span class="sxs-lookup"><span data-stu-id="b3a4f-120">-Table</span></span>
<span data-ttu-id="b3a4f-121">Azure depolama tablosu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3a4f-121">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="b3a4f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3a4f-122">CommonParameters</span></span>
<span data-ttu-id="b3a4f-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3a4f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3a4f-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3a4f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3a4f-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3a4f-125">INPUTS</span></span>

### <span data-ttu-id="b3a4f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b3a4f-126">System.String</span></span>

### <span data-ttu-id="b3a4f-127">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="b3a4f-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b3a4f-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3a4f-128">OUTPUTS</span></span>

### <span data-ttu-id="b3a4f-129">Microsoft. Windowsazde. Storage. Table. SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="b3a4f-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="b3a4f-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3a4f-130">NOTES</span></span>

## <span data-ttu-id="b3a4f-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3a4f-131">RELATED LINKS</span></span>

[<span data-ttu-id="b3a4f-132">Yeni-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b3a4f-132">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b3a4f-133">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b3a4f-133">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b3a4f-134">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b3a4f-134">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b3a4f-135">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b3a4f-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


