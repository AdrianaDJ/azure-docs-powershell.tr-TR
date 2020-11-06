---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/new-azurermstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
ms.openlocfilehash: e44ccbaae730554db35610ff1084e9740e873e53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594330"
---
# <span data-ttu-id="ae13f-101">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ae13f-101">New-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="ae13f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae13f-102">SYNOPSIS</span></span>
<span data-ttu-id="ae13f-103">Azure depolama hesabı için depolama anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ae13f-103">Regenerates a storage key for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae13f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ae13f-104">SYNTAX</span></span>

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae13f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ae13f-105">DESCRIPTION</span></span>
<span data-ttu-id="ae13f-106">**Yeni-AzureRmStorageAccountKey** cmdlet 'ı Azure depolama hesabı için depolama anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ae13f-106">The **New-AzureRmStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="ae13f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ae13f-107">EXAMPLES</span></span>

### <span data-ttu-id="ae13f-108">Örnek 1: depolama anahtarını yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="ae13f-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzureRmStorageKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="ae13f-109">Bu komut belirtilen depolama hesabının depolama anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ae13f-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="ae13f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ae13f-110">PARAMETERS</span></span>

### <span data-ttu-id="ae13f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae13f-111">-DefaultProfile</span></span>
<span data-ttu-id="ae13f-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ae13f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae13f-113">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="ae13f-113">-KeyName</span></span>
<span data-ttu-id="ae13f-114">Hangi tuşun yeniden yeniden kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae13f-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="ae13f-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ae13f-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ae13f-116">anahtar</span><span class="sxs-lookup"><span data-stu-id="ae13f-116">key1</span></span>
- <span data-ttu-id="ae13f-117">anahtar2</span><span class="sxs-lookup"><span data-stu-id="ae13f-117">key2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae13f-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="ae13f-118">-Name</span></span>
<span data-ttu-id="ae13f-119">Depolama anahtarının yeniden oluşturulacak depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae13f-119">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae13f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae13f-120">-ResourceGroupName</span></span>
<span data-ttu-id="ae13f-121">Depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae13f-121">Specifies the name of the resource group that contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae13f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae13f-122">CommonParameters</span></span>
<span data-ttu-id="ae13f-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ae13f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae13f-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae13f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae13f-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ae13f-125">INPUTS</span></span>

### <span data-ttu-id="ae13f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ae13f-126">System.String</span></span>

## <span data-ttu-id="ae13f-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ae13f-127">OUTPUTS</span></span>

### <span data-ttu-id="ae13f-128">Microsoft. Azure. Management. Storage. model. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ae13f-128">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="ae13f-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ae13f-129">NOTES</span></span>

## <span data-ttu-id="ae13f-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ae13f-130">RELATED LINKS</span></span>

[<span data-ttu-id="ae13f-131">Get-azurermstorageın</span><span class="sxs-lookup"><span data-stu-id="ae13f-131">Get-AzureRmStorageAccountKey</span></span>](./Get-AzureRmStorageAccountKey.md)
