---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: f260af1bc26d9cf921a26e4f08c3c4feab4b79c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590765"
---
# <span data-ttu-id="31261-101">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="31261-101">Get-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="31261-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31261-102">SYNOPSIS</span></span>
<span data-ttu-id="31261-103">Bir toplu Iş hesabındaki uygulama paketi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="31261-103">Gets information about an application package in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31261-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="31261-104">SYNTAX</span></span>

```
Get-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31261-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="31261-105">DESCRIPTION</span></span>
<span data-ttu-id="31261-106">**Get-AzureRmBatchApplicationPackage** cmdlet 'i, bir Azure toplu hesabındaki uygulama paketi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="31261-106">The **Get-AzureRmBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="31261-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="31261-107">EXAMPLES</span></span>

### <span data-ttu-id="31261-108">Örnek 1: bir toplu Iş hesabındaki uygulama paketinin ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="31261-108">Example 1: Get details of an application package in a Batch account</span></span>
```
PS C:\>Get-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0"
Format             : zip
State              : Active
Version            : 1.0
LastActivationTime : 13/05/2016 4:03:24 AM
StorageUrl         : https://contosobatch.blob.core.windows.net/app-test
StorageUrlExpiry   : 13/05/2016 8:04:44 AM
Id                 : litware
```

<span data-ttu-id="31261-109">Bu komut, Litwin paketinin 1,0 sürümündeki ayrıntıları alır.</span><span class="sxs-lookup"><span data-stu-id="31261-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="31261-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="31261-110">PARAMETERS</span></span>

### <span data-ttu-id="31261-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="31261-111">-AccountName</span></span>
<span data-ttu-id="31261-112">Bu cmdlet 'in bilgi aldığı toplu Iş hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="31261-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="31261-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="31261-113">-ApplicationId</span></span>
<span data-ttu-id="31261-114">Uygulamanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="31261-114">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31261-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="31261-115">-ApplicationVersion</span></span>
<span data-ttu-id="31261-116">Uygulamanın sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="31261-116">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31261-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31261-117">-ResourceGroupName</span></span>
<span data-ttu-id="31261-118">Toplu Iş hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="31261-118">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31261-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31261-119">-DefaultProfile</span></span>
<span data-ttu-id="31261-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="31261-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31261-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31261-121">CommonParameters</span></span>
<span data-ttu-id="31261-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="31261-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31261-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31261-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31261-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="31261-124">INPUTS</span></span>

## <span data-ttu-id="31261-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="31261-125">OUTPUTS</span></span>

### <span data-ttu-id="31261-126">Microsoft.Azure.Commands.Batch. Modeller. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="31261-126">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="31261-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="31261-127">NOTES</span></span>

## <span data-ttu-id="31261-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="31261-128">RELATED LINKS</span></span>

[<span data-ttu-id="31261-129">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="31261-129">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="31261-130">Yeni-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="31261-130">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="31261-131">Yeni-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="31261-131">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="31261-132">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="31261-132">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="31261-133">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="31261-133">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="31261-134">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="31261-134">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


