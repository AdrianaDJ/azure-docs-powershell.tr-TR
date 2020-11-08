---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: d63c948e59dbc05122c63b6688277a7015a42163
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098623"
---
# <span data-ttu-id="23dff-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="23dff-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="23dff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23dff-102">SYNOPSIS</span></span>
<span data-ttu-id="23dff-103">Azure depolama hesabı için depolama anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="23dff-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="23dff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="23dff-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23dff-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="23dff-105">DESCRIPTION</span></span>
<span data-ttu-id="23dff-106">**New-AzStorageAccountKey** cmdlet 'ı Azure depolama hesabı için depolama anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="23dff-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="23dff-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="23dff-107">EXAMPLES</span></span>

### <span data-ttu-id="23dff-108">Örnek 1: depolama anahtarını yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="23dff-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageAccountKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="23dff-109">Bu komut belirtilen depolama hesabının depolama anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="23dff-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="23dff-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="23dff-110">PARAMETERS</span></span>

### <span data-ttu-id="23dff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23dff-111">-DefaultProfile</span></span>
<span data-ttu-id="23dff-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="23dff-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23dff-113">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="23dff-113">-KeyName</span></span>
<span data-ttu-id="23dff-114">Hangi tuşun yeniden yeniden kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="23dff-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="23dff-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="23dff-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="23dff-116">anahtar</span><span class="sxs-lookup"><span data-stu-id="23dff-116">key1</span></span>
- <span data-ttu-id="23dff-117">anahtar2</span><span class="sxs-lookup"><span data-stu-id="23dff-117">key2</span></span>

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

### <span data-ttu-id="23dff-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="23dff-118">-Name</span></span>
<span data-ttu-id="23dff-119">Depolama anahtarının yeniden oluşturulacak depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="23dff-119">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="23dff-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23dff-120">-ResourceGroupName</span></span>
<span data-ttu-id="23dff-121">Depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="23dff-121">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="23dff-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23dff-122">CommonParameters</span></span>
<span data-ttu-id="23dff-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="23dff-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23dff-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23dff-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23dff-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="23dff-125">INPUTS</span></span>

### <span data-ttu-id="23dff-126">System. String</span><span class="sxs-lookup"><span data-stu-id="23dff-126">System.String</span></span>

## <span data-ttu-id="23dff-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="23dff-127">OUTPUTS</span></span>

### <span data-ttu-id="23dff-128">Microsoft. Azure. Management. Storage. modeller. StorageAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="23dff-128">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span></span>

## <span data-ttu-id="23dff-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="23dff-129">NOTES</span></span>

## <span data-ttu-id="23dff-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="23dff-130">RELATED LINKS</span></span>

[<span data-ttu-id="23dff-131">Get-Azdepolama anahtarı</span><span class="sxs-lookup"><span data-stu-id="23dff-131">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)
