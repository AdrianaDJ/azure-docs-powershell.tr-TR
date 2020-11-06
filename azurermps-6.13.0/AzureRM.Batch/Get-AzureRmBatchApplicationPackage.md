---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: 5e0be2a9c9ba56fecee9e7c1e7ae37a3e39be110
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589592"
---
# <span data-ttu-id="670fc-101">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="670fc-101">Get-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="670fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="670fc-102">SYNOPSIS</span></span>
<span data-ttu-id="670fc-103">Bir toplu Iş hesabındaki uygulama paketi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="670fc-103">Gets information about an application package in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="670fc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="670fc-104">SYNTAX</span></span>

```
Get-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="670fc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="670fc-105">DESCRIPTION</span></span>
<span data-ttu-id="670fc-106">**Get-AzureRmBatchApplicationPackage** cmdlet 'i, bir Azure toplu hesabındaki uygulama paketi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="670fc-106">The **Get-AzureRmBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="670fc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="670fc-107">EXAMPLES</span></span>

### <span data-ttu-id="670fc-108">Örnek 1: bir toplu Iş hesabındaki uygulama paketinin ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="670fc-108">Example 1: Get details of an application package in a Batch account</span></span>
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

<span data-ttu-id="670fc-109">Bu komut, Litwin paketinin 1,0 sürümündeki ayrıntıları alır.</span><span class="sxs-lookup"><span data-stu-id="670fc-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="670fc-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="670fc-110">PARAMETERS</span></span>

### <span data-ttu-id="670fc-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="670fc-111">-AccountName</span></span>
<span data-ttu-id="670fc-112">Bu cmdlet 'in bilgi aldığı toplu Iş hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="670fc-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="670fc-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="670fc-113">-ApplicationId</span></span>
<span data-ttu-id="670fc-114">Uygulamanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="670fc-114">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="670fc-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="670fc-115">-ApplicationVersion</span></span>
<span data-ttu-id="670fc-116">Uygulamanın sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="670fc-116">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="670fc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="670fc-117">-DefaultProfile</span></span>
<span data-ttu-id="670fc-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="670fc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="670fc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="670fc-119">-ResourceGroupName</span></span>
<span data-ttu-id="670fc-120">Toplu Iş hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="670fc-120">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="670fc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="670fc-121">CommonParameters</span></span>
<span data-ttu-id="670fc-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="670fc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="670fc-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="670fc-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="670fc-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="670fc-124">INPUTS</span></span>

### <span data-ttu-id="670fc-125">System. String</span><span class="sxs-lookup"><span data-stu-id="670fc-125">System.String</span></span>

## <span data-ttu-id="670fc-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="670fc-126">OUTPUTS</span></span>

### <span data-ttu-id="670fc-127">Microsoft.Azure.Commands.Batch. Modeller. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="670fc-127">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="670fc-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="670fc-128">NOTES</span></span>

## <span data-ttu-id="670fc-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="670fc-129">RELATED LINKS</span></span>

[<span data-ttu-id="670fc-130">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="670fc-130">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="670fc-131">Yeni-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="670fc-131">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="670fc-132">Yeni-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="670fc-132">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="670fc-133">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="670fc-133">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="670fc-134">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="670fc-134">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="670fc-135">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="670fc-135">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


