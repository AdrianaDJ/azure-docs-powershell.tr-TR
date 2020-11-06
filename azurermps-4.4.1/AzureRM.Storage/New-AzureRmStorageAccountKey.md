---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
ms.openlocfilehash: 76b7ea9eb4a248071025ef359d6bf0877b35fe89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594982"
---
# <span data-ttu-id="11d6c-101">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="11d6c-101">New-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="11d6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11d6c-102">SYNOPSIS</span></span>
<span data-ttu-id="11d6c-103">Azure depolama hesabı için depolama anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="11d6c-103">Regenerates a storage key for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11d6c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="11d6c-104">SYNTAX</span></span>

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11d6c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="11d6c-105">DESCRIPTION</span></span>
<span data-ttu-id="11d6c-106">**Yeni-AzureRmStorageAccountKey** cmdlet 'ı Azure depolama hesabı için depolama anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="11d6c-106">The **New-AzureRmStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="11d6c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="11d6c-107">EXAMPLES</span></span>

### <span data-ttu-id="11d6c-108">Örnek 1: depolama anahtarını yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="11d6c-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzureRmStorageAccountKey -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -KeyName "key1"
```

<span data-ttu-id="11d6c-109">Bu komut belirtilen depolama hesabının depolama anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="11d6c-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="11d6c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="11d6c-110">PARAMETERS</span></span>

### <span data-ttu-id="11d6c-111">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="11d6c-111">-KeyName</span></span>
<span data-ttu-id="11d6c-112">Hangi tuşun yeniden yeniden kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="11d6c-112">Specifies which key to regenerate.</span></span>
<span data-ttu-id="11d6c-113">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="11d6c-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="11d6c-114">anahtar</span><span class="sxs-lookup"><span data-stu-id="11d6c-114">key1</span></span> 
- <span data-ttu-id="11d6c-115">anahtar2</span><span class="sxs-lookup"><span data-stu-id="11d6c-115">key2</span></span>

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

### <span data-ttu-id="11d6c-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="11d6c-116">-Name</span></span>
<span data-ttu-id="11d6c-117">Depolama anahtarının yeniden oluşturulacak depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="11d6c-117">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="11d6c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11d6c-118">-ResourceGroupName</span></span>
<span data-ttu-id="11d6c-119">Depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="11d6c-119">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="11d6c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11d6c-120">-DefaultProfile</span></span>
<span data-ttu-id="11d6c-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="11d6c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11d6c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11d6c-122">CommonParameters</span></span>
<span data-ttu-id="11d6c-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="11d6c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11d6c-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11d6c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11d6c-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="11d6c-125">INPUTS</span></span>

## <span data-ttu-id="11d6c-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="11d6c-126">OUTPUTS</span></span>

## <span data-ttu-id="11d6c-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="11d6c-127">NOTES</span></span>

## <span data-ttu-id="11d6c-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="11d6c-128">RELATED LINKS</span></span>

[<span data-ttu-id="11d6c-129">Get-azurermstorageın</span><span class="sxs-lookup"><span data-stu-id="11d6c-129">Get-AzureRmStorageAccountKey</span></span>](./Get-AzureRmStorageAccountKey.md)


