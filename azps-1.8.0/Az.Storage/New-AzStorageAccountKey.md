---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: 05bd6c804d359a06e83f25922263bdfdb55acc73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758628"
---
# <span data-ttu-id="10204-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="10204-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="10204-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10204-102">SYNOPSIS</span></span>
<span data-ttu-id="10204-103">Azure depolama hesabı için depolama anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="10204-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="10204-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="10204-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10204-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="10204-105">DESCRIPTION</span></span>
<span data-ttu-id="10204-106">**New-AzStorageAccountKey** cmdlet 'ı Azure depolama hesabı için depolama anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="10204-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="10204-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="10204-107">EXAMPLES</span></span>

### <span data-ttu-id="10204-108">Örnek 1: depolama anahtarını yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="10204-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageAccountKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="10204-109">Bu komut belirtilen depolama hesabının depolama anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="10204-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="10204-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="10204-110">PARAMETERS</span></span>

### <span data-ttu-id="10204-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10204-111">-DefaultProfile</span></span>
<span data-ttu-id="10204-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="10204-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10204-113">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="10204-113">-KeyName</span></span>
<span data-ttu-id="10204-114">Hangi tuşun yeniden yeniden kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10204-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="10204-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="10204-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="10204-116">anahtar</span><span class="sxs-lookup"><span data-stu-id="10204-116">key1</span></span>
- <span data-ttu-id="10204-117">anahtar2</span><span class="sxs-lookup"><span data-stu-id="10204-117">key2</span></span>

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

### <span data-ttu-id="10204-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="10204-118">-Name</span></span>
<span data-ttu-id="10204-119">Depolama anahtarının yeniden oluşturulacak depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10204-119">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="10204-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10204-120">-ResourceGroupName</span></span>
<span data-ttu-id="10204-121">Depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10204-121">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="10204-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10204-122">CommonParameters</span></span>
<span data-ttu-id="10204-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="10204-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10204-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10204-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10204-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="10204-125">INPUTS</span></span>

### <span data-ttu-id="10204-126">System. String</span><span class="sxs-lookup"><span data-stu-id="10204-126">System.String</span></span>

## <span data-ttu-id="10204-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="10204-127">OUTPUTS</span></span>

### <span data-ttu-id="10204-128">Microsoft. Azure. Management. Storage. model. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="10204-128">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="10204-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="10204-129">NOTES</span></span>

## <span data-ttu-id="10204-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="10204-130">RELATED LINKS</span></span>

[<span data-ttu-id="10204-131">Get-Azdepolama anahtarı</span><span class="sxs-lookup"><span data-stu-id="10204-131">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)
