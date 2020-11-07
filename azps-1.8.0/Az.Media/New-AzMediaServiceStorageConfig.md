---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/new-azmediaservicestorageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
ms.openlocfilehash: 8fb6e4a683decc8b5615a7cf0c8088681578f8ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915763"
---
# <span data-ttu-id="858fb-101">New-AzMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="858fb-101">New-AzMediaServiceStorageConfig</span></span>

## <span data-ttu-id="858fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="858fb-102">SYNOPSIS</span></span>
<span data-ttu-id="858fb-103">Medya hizmeti cmdlet 'leri için depolama hesabı yapılandırması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="858fb-103">Create a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="858fb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="858fb-104">SYNTAX</span></span>

```
New-AzMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="858fb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="858fb-105">DESCRIPTION</span></span>
<span data-ttu-id="858fb-106">**Yeni-AzMediaServiceStorageConfig** cmdlet 'i, medya hizmeti cmdlet 'leri için bir depolama hesabı yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="858fb-106">The **New-AzMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="858fb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="858fb-107">EXAMPLES</span></span>

### <span data-ttu-id="858fb-108">Örnek 1: medya hizmeti cmdlet 'lerinin depolama hesabı yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="858fb-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="858fb-109">İlk komut, **New-AzStorageAccount** cmdlet 'ini kullanarak bir depolama hesabı nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="858fb-109">The first command creates a storage account object by using **the New-AzStorageAccount** cmdlet.</span></span>
<span data-ttu-id="858fb-110">Bu depolama hesabının Storage1 komut adları ve türü Standard_GRS olarak adlandırılır ve sonucu $StorageAccount adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="858fb-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="858fb-111">İkinci komut, $StorageAccount değişkeninde depolanan depolama hesabı KIMLIĞI bilgilerini kullanarak medya hizmetiyle ilişkili birincil depolama hesabı olarak bir depolama yapılandırması nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="858fb-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="858fb-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="858fb-112">PARAMETERS</span></span>

### <span data-ttu-id="858fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="858fb-113">-DefaultProfile</span></span>
<span data-ttu-id="858fb-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="858fb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="858fb-115">-IsPrimary</span><span class="sxs-lookup"><span data-stu-id="858fb-115">-IsPrimary</span></span>
<span data-ttu-id="858fb-116">Cmdlet 'in depolama hesabını medya hizmeti için birincil depolama alanı olarak oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="858fb-116">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

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

### <span data-ttu-id="858fb-117">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="858fb-117">-StorageAccountId</span></span>
<span data-ttu-id="858fb-118">Depolama hesabının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="858fb-118">Specifies the ID of the storage account.</span></span>

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

### <span data-ttu-id="858fb-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="858fb-119">-Confirm</span></span>
<span data-ttu-id="858fb-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="858fb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="858fb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="858fb-121">-WhatIf</span></span>
<span data-ttu-id="858fb-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="858fb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="858fb-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="858fb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="858fb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="858fb-124">CommonParameters</span></span>
<span data-ttu-id="858fb-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="858fb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="858fb-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="858fb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="858fb-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="858fb-127">INPUTS</span></span>

### <span data-ttu-id="858fb-128">System. String</span><span class="sxs-lookup"><span data-stu-id="858fb-128">System.String</span></span>

## <span data-ttu-id="858fb-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="858fb-129">OUTPUTS</span></span>

### <span data-ttu-id="858fb-130">Microsoft. Azure. Commands. Media. modeller. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="858fb-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="858fb-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="858fb-131">NOTES</span></span>

## <span data-ttu-id="858fb-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="858fb-132">RELATED LINKS</span></span>

[<span data-ttu-id="858fb-133">Sync-AzMediaServiceStorageKeys</span><span class="sxs-lookup"><span data-stu-id="858fb-133">Sync-AzMediaServiceStorageKeys</span></span>](./Sync-AzMediaServiceStorageKeys.md)

