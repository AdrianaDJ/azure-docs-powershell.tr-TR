---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: 70acc17513e60892baae1fe8ebc15776518b3f57
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936237"
---
# <span data-ttu-id="27c5a-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="27c5a-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="27c5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27c5a-102">SYNOPSIS</span></span>
<span data-ttu-id="27c5a-103">Azure depolama hesabı için depolama anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="27c5a-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="27c5a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="27c5a-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27c5a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="27c5a-105">DESCRIPTION</span></span>
<span data-ttu-id="27c5a-106">**New-AzStorageAccountKey** cmdlet 'ı Azure depolama hesabı için depolama anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="27c5a-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="27c5a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="27c5a-107">EXAMPLES</span></span>

### <span data-ttu-id="27c5a-108">Örnek 1: depolama anahtarını yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="27c5a-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="27c5a-109">Bu komut belirtilen depolama hesabının depolama anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="27c5a-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="27c5a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="27c5a-110">PARAMETERS</span></span>

### <span data-ttu-id="27c5a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27c5a-111">-DefaultProfile</span></span>
<span data-ttu-id="27c5a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="27c5a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27c5a-113">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="27c5a-113">-KeyName</span></span>
<span data-ttu-id="27c5a-114">Hangi tuşun yeniden yeniden kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27c5a-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="27c5a-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="27c5a-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="27c5a-116">anahtar</span><span class="sxs-lookup"><span data-stu-id="27c5a-116">key1</span></span>
- <span data-ttu-id="27c5a-117">anahtar2</span><span class="sxs-lookup"><span data-stu-id="27c5a-117">key2</span></span>

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

### <span data-ttu-id="27c5a-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="27c5a-118">-Name</span></span>
<span data-ttu-id="27c5a-119">Depolama anahtarının yeniden oluşturulacak depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27c5a-119">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="27c5a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27c5a-120">-ResourceGroupName</span></span>
<span data-ttu-id="27c5a-121">Depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27c5a-121">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="27c5a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27c5a-122">CommonParameters</span></span>
<span data-ttu-id="27c5a-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="27c5a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27c5a-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27c5a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27c5a-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="27c5a-125">INPUTS</span></span>

### <span data-ttu-id="27c5a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="27c5a-126">System.String</span></span>

## <span data-ttu-id="27c5a-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="27c5a-127">OUTPUTS</span></span>

### <span data-ttu-id="27c5a-128">Microsoft. Azure. Management. Storage. model. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="27c5a-128">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="27c5a-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="27c5a-129">NOTES</span></span>

## <span data-ttu-id="27c5a-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="27c5a-130">RELATED LINKS</span></span>

[<span data-ttu-id="27c5a-131">Get-Azdepolama anahtarı</span><span class="sxs-lookup"><span data-stu-id="27c5a-131">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)
