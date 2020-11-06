---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaServiceStorageConfig.md
ms.openlocfilehash: 236486af937a99812f4979ed4db089002fb9ad30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592610"
---
# <span data-ttu-id="0c2fb-101">New-AzureRmMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="0c2fb-101">New-AzureRmMediaServiceStorageConfig</span></span>

## <span data-ttu-id="0c2fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c2fb-102">SYNOPSIS</span></span>
<span data-ttu-id="0c2fb-103">Medya hizmeti cmdlet 'leri için depolama hesabı yapılandırması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0c2fb-103">Create a storage account configuration for the media service cmdlets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c2fb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c2fb-104">SYNTAX</span></span>

```
New-AzureRmMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c2fb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c2fb-105">DESCRIPTION</span></span>
<span data-ttu-id="0c2fb-106">**Yeni-AzureRmMediaServiceStorageConfig** cmdlet 'i medya hizmeti cmdlet 'lerinin depolama hesabı yapılandırmasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0c2fb-106">The **New-AzureRmMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="0c2fb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c2fb-107">EXAMPLES</span></span>

### <span data-ttu-id="0c2fb-108">Örnek 1: medya hizmeti cmdlet 'lerinin depolama hesabı yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="0c2fb-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="0c2fb-109">İlk komut, **New-AzureRmStorageAccount** cmdlet 'ini kullanarak bir depolama hesabı nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0c2fb-109">The first command creates a storage account object by using **the New-AzureRmStorageAccount** cmdlet.</span></span>
<span data-ttu-id="0c2fb-110">Bu depolama hesabının Storage1 komut adları ve türü Standard_GRS olarak adlandırılır ve sonucu $StorageAccount adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="0c2fb-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>

<span data-ttu-id="0c2fb-111">İkinci komut, $StorageAccount değişkeninde depolanan depolama hesabı KIMLIĞI bilgilerini kullanarak medya hizmetiyle ilişkili birincil depolama hesabı olarak bir depolama yapılandırması nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0c2fb-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="0c2fb-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c2fb-112">PARAMETERS</span></span>

### <span data-ttu-id="0c2fb-113">-IsPrimary</span><span class="sxs-lookup"><span data-stu-id="0c2fb-113">-IsPrimary</span></span>
<span data-ttu-id="0c2fb-114">Cmdlet 'in depolama hesabını medya hizmeti için birincil depolama alanı olarak oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="0c2fb-114">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c2fb-115">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="0c2fb-115">-StorageAccountId</span></span>
<span data-ttu-id="0c2fb-116">Depolama hesabının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c2fb-116">Specifies the ID of the storage account.</span></span>

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

### <span data-ttu-id="0c2fb-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="0c2fb-117">-Confirm</span></span>
<span data-ttu-id="0c2fb-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0c2fb-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c2fb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c2fb-119">-WhatIf</span></span>
<span data-ttu-id="0c2fb-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0c2fb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c2fb-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0c2fb-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c2fb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c2fb-122">-DefaultProfile</span></span>
<span data-ttu-id="0c2fb-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0c2fb-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c2fb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c2fb-124">CommonParameters</span></span>
<span data-ttu-id="0c2fb-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c2fb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c2fb-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c2fb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c2fb-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c2fb-127">INPUTS</span></span>

## <span data-ttu-id="0c2fb-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c2fb-128">OUTPUTS</span></span>

### <span data-ttu-id="0c2fb-129">Microsoft. Azure. Commands. Media. modeller. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0c2fb-129">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="0c2fb-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c2fb-130">NOTES</span></span>

## <span data-ttu-id="0c2fb-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c2fb-131">RELATED LINKS</span></span>

[<span data-ttu-id="0c2fb-132">Sync-AzureRmMediaServiceStorageKeys</span><span class="sxs-lookup"><span data-stu-id="0c2fb-132">Sync-AzureRmMediaServiceStorageKeys</span></span>](./Sync-AzureRmMediaServiceStorageKeys.md)


