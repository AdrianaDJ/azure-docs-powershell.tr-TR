---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: eebf58120449466ac18231af6daed538ff7da937
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277188"
---
# <span data-ttu-id="d56e0-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d56e0-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="d56e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d56e0-102">SYNOPSIS</span></span>
<span data-ttu-id="d56e0-103">Azure depolama hesabı için depolama anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d56e0-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="d56e0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d56e0-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d56e0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d56e0-105">DESCRIPTION</span></span>
<span data-ttu-id="d56e0-106">**New-AzStorageAccountKey** cmdlet 'ı Azure depolama hesabı için depolama anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d56e0-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="d56e0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d56e0-107">EXAMPLES</span></span>

### <span data-ttu-id="d56e0-108">Örnek 1: depolama anahtarını yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="d56e0-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageAccountKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="d56e0-109">Bu komut belirtilen depolama hesabının depolama anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d56e0-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="d56e0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d56e0-110">PARAMETERS</span></span>

### <span data-ttu-id="d56e0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d56e0-111">-DefaultProfile</span></span>
<span data-ttu-id="d56e0-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d56e0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d56e0-113">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="d56e0-113">-KeyName</span></span>
<span data-ttu-id="d56e0-114">Hangi tuşun yeniden yeniden kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d56e0-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="d56e0-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d56e0-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d56e0-116">anahtar</span><span class="sxs-lookup"><span data-stu-id="d56e0-116">key1</span></span>
- <span data-ttu-id="d56e0-117">anahtar2</span><span class="sxs-lookup"><span data-stu-id="d56e0-117">key2</span></span>
- <span data-ttu-id="d56e0-118">kerb1</span><span class="sxs-lookup"><span data-stu-id="d56e0-118">kerb1</span></span>
- <span data-ttu-id="d56e0-119">kerb2</span><span class="sxs-lookup"><span data-stu-id="d56e0-119">kerb2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2, kerb1, kerb2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d56e0-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="d56e0-120">-Name</span></span>
<span data-ttu-id="d56e0-121">Depolama anahtarının yeniden oluşturulacak depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d56e0-121">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="d56e0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d56e0-122">-ResourceGroupName</span></span>
<span data-ttu-id="d56e0-123">Depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d56e0-123">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="d56e0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d56e0-124">CommonParameters</span></span>
<span data-ttu-id="d56e0-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d56e0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d56e0-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d56e0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d56e0-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d56e0-127">INPUTS</span></span>

### <span data-ttu-id="d56e0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d56e0-128">System.String</span></span>

## <span data-ttu-id="d56e0-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d56e0-129">OUTPUTS</span></span>

### <span data-ttu-id="d56e0-130">Microsoft. Azure. Management. Storage. modeller. StorageAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="d56e0-130">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span></span>

## <span data-ttu-id="d56e0-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d56e0-131">NOTES</span></span>

## <span data-ttu-id="d56e0-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d56e0-132">RELATED LINKS</span></span>

[<span data-ttu-id="d56e0-133">Get-Azdepolama anahtarı</span><span class="sxs-lookup"><span data-stu-id="d56e0-133">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)
