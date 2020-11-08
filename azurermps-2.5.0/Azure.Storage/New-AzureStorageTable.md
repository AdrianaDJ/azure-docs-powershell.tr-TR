---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetable
schema: 2.0.0
ms.openlocfilehash: 4fe02c9824945593de4b4160e9db10b1573a335a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939442"
---
# <span data-ttu-id="8a42f-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="8a42f-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="8a42f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a42f-102">SYNOPSIS</span></span>
<span data-ttu-id="8a42f-103">Depolama tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a42f-103">Creates a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a42f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8a42f-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a42f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8a42f-105">DESCRIPTION</span></span>
<span data-ttu-id="8a42f-106">**New-AzureStorageTable** cmdlet 'ı, Azure 'daki depolama hesabıyla ilişkilendirilmiş bir depolama tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a42f-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="8a42f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8a42f-107">EXAMPLES</span></span>

### <span data-ttu-id="8a42f-108">Örnek 1: Azure depolama tablosu oluşturma</span><span class="sxs-lookup"><span data-stu-id="8a42f-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="8a42f-109">Bu komut, tableabc adında bir depolama tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a42f-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="8a42f-110">Örnek 2: birden çok Azure depolama tablosu oluşturma</span><span class="sxs-lookup"><span data-stu-id="8a42f-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="8a42f-111">Bu komut birden çok tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a42f-111">This command creates multiple tables.</span></span>
<span data-ttu-id="8a42f-112">.NET **String** sınıfının **bölme** yöntemini kullanır ve sonra da ardışık düzene geçirir.</span><span class="sxs-lookup"><span data-stu-id="8a42f-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="8a42f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8a42f-113">PARAMETERS</span></span>

### <span data-ttu-id="8a42f-114">-Context</span><span class="sxs-lookup"><span data-stu-id="8a42f-114">-Context</span></span>
<span data-ttu-id="8a42f-115">Depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a42f-115">Specifies the storage context.</span></span>
<span data-ttu-id="8a42f-116">Bunu oluşturmak için New-AzureStorageContext cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8a42f-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8a42f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a42f-117">-DefaultProfile</span></span>
<span data-ttu-id="8a42f-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8a42f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a42f-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="8a42f-119">-Name</span></span>
<span data-ttu-id="8a42f-120">Yeni tablo için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a42f-120">Specifies a name for the new table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a42f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a42f-121">CommonParameters</span></span>
<span data-ttu-id="8a42f-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8a42f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a42f-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a42f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a42f-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8a42f-124">INPUTS</span></span>

### <span data-ttu-id="8a42f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="8a42f-125">System.String</span></span>

### <span data-ttu-id="8a42f-126">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="8a42f-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8a42f-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8a42f-127">OUTPUTS</span></span>

### <span data-ttu-id="8a42f-128">Microsoft. Windowsazde. Commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="8a42f-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="8a42f-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8a42f-129">NOTES</span></span>

## <span data-ttu-id="8a42f-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8a42f-130">RELATED LINKS</span></span>

[<span data-ttu-id="8a42f-131">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="8a42f-131">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="8a42f-132">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="8a42f-132">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)

