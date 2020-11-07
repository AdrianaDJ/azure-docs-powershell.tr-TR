---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/new-azurermmediaservicestorageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaServiceStorageConfig.md
ms.openlocfilehash: efc157e2e4395055d1af2ef80f0a9fcc98886d15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764638"
---
# <span data-ttu-id="cf062-101">New-AzureRmMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="cf062-101">New-AzureRmMediaServiceStorageConfig</span></span>

## <span data-ttu-id="cf062-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf062-102">SYNOPSIS</span></span>
<span data-ttu-id="cf062-103">Medya hizmeti cmdlet 'leri için depolama hesabı yapılandırması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="cf062-103">Create a storage account configuration for the media service cmdlets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf062-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cf062-104">SYNTAX</span></span>

```
New-AzureRmMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf062-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cf062-105">DESCRIPTION</span></span>
<span data-ttu-id="cf062-106">**Yeni-AzureRmMediaServiceStorageConfig** cmdlet 'i medya hizmeti cmdlet 'lerinin depolama hesabı yapılandırmasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cf062-106">The **New-AzureRmMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="cf062-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cf062-107">EXAMPLES</span></span>

### <span data-ttu-id="cf062-108">Örnek 1: medya hizmeti cmdlet 'lerinin depolama hesabı yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="cf062-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="cf062-109">İlk komut, **New-AzureRmStorageAccount** cmdlet 'ini kullanarak bir depolama hesabı nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cf062-109">The first command creates a storage account object by using **the New-AzureRmStorageAccount** cmdlet.</span></span>
<span data-ttu-id="cf062-110">Bu depolama hesabının Storage1 komut adları ve türü Standard_GRS olarak adlandırılır ve sonucu $StorageAccount adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="cf062-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="cf062-111">İkinci komut, $StorageAccount değişkeninde depolanan depolama hesabı KIMLIĞI bilgilerini kullanarak medya hizmetiyle ilişkili birincil depolama hesabı olarak bir depolama yapılandırması nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cf062-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="cf062-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cf062-112">PARAMETERS</span></span>

### <span data-ttu-id="cf062-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf062-113">-DefaultProfile</span></span>
<span data-ttu-id="cf062-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="cf062-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf062-115">-IsPrimary</span><span class="sxs-lookup"><span data-stu-id="cf062-115">-IsPrimary</span></span>
<span data-ttu-id="cf062-116">Cmdlet 'in depolama hesabını medya hizmeti için birincil depolama alanı olarak oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="cf062-116">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

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

### <span data-ttu-id="cf062-117">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="cf062-117">-StorageAccountId</span></span>
<span data-ttu-id="cf062-118">Depolama hesabının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf062-118">Specifies the ID of the storage account.</span></span>

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

### <span data-ttu-id="cf062-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="cf062-119">-Confirm</span></span>
<span data-ttu-id="cf062-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cf062-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf062-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf062-121">-WhatIf</span></span>
<span data-ttu-id="cf062-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cf062-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf062-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cf062-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf062-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf062-124">CommonParameters</span></span>
<span data-ttu-id="cf062-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cf062-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf062-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf062-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf062-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cf062-127">INPUTS</span></span>

### <span data-ttu-id="cf062-128">System. String</span><span class="sxs-lookup"><span data-stu-id="cf062-128">System.String</span></span>

## <span data-ttu-id="cf062-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cf062-129">OUTPUTS</span></span>

### <span data-ttu-id="cf062-130">Microsoft. Azure. Commands. Media. modeller. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cf062-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="cf062-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cf062-131">NOTES</span></span>

## <span data-ttu-id="cf062-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cf062-132">RELATED LINKS</span></span>

[<span data-ttu-id="cf062-133">Sync-AzureRmMediaServiceStorageKeys</span><span class="sxs-lookup"><span data-stu-id="cf062-133">Sync-AzureRmMediaServiceStorageKeys</span></span>](./Sync-AzureRmMediaServiceStorageKeys.md)


