---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
ms.openlocfilehash: e5e289679327b0376530f01f91310cf211465e48
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104139"
---
# <span data-ttu-id="a0198-101">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a0198-101">Get-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="a0198-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0198-102">SYNOPSIS</span></span>
<span data-ttu-id="a0198-103">Bir toplu Iş hesabındaki uygulama paketi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="a0198-103">Gets information about an application package in a Batch account.</span></span>

## <span data-ttu-id="a0198-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0198-104">SYNTAX</span></span>

```
Get-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-ApplicationVersion] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0198-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0198-105">DESCRIPTION</span></span>
<span data-ttu-id="a0198-106">**Get-AzBatchApplicationPackage** cmdlet 'i, bir Azure toplu hesabındaki uygulama paketi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="a0198-106">The **Get-AzBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="a0198-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0198-107">EXAMPLES</span></span>

### <span data-ttu-id="a0198-108">Örnek 1: bir toplu Iş hesabındaki uygulama paketinin ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="a0198-108">Example 1: Get details of an application package in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -ApplicationVersion "1.0"
Format             : zip
State              : Active
Version            : 1.0
LastActivationTime : 13/05/2016 4:03:24 AM
StorageUrl         : https://contosobatch.blob.core.windows.net/app-test
StorageUrlExpiry   : 13/05/2016 8:04:44 AM
Id                 : litware
```

<span data-ttu-id="a0198-109">Bu komut, Litwin paketinin 1,0 sürümündeki ayrıntıları alır.</span><span class="sxs-lookup"><span data-stu-id="a0198-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="a0198-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0198-110">PARAMETERS</span></span>

### <span data-ttu-id="a0198-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a0198-111">-AccountName</span></span>
<span data-ttu-id="a0198-112">Bu cmdlet 'in bilgi aldığı toplu Iş hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0198-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="a0198-113">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="a0198-113">-ApplicationName</span></span>
<span data-ttu-id="a0198-114">Uygulamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0198-114">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0198-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="a0198-115">-ApplicationVersion</span></span>
<span data-ttu-id="a0198-116">Uygulamanın sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0198-116">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0198-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0198-117">-DefaultProfile</span></span>
<span data-ttu-id="a0198-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a0198-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0198-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0198-119">-ResourceGroupName</span></span>
<span data-ttu-id="a0198-120">Toplu Iş hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0198-120">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="a0198-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0198-121">CommonParameters</span></span>
<span data-ttu-id="a0198-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0198-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0198-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a0198-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0198-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0198-124">INPUTS</span></span>

### <span data-ttu-id="a0198-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a0198-125">System.String</span></span>

## <span data-ttu-id="a0198-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0198-126">OUTPUTS</span></span>

### <span data-ttu-id="a0198-127">Microsoft.Azure.Commands.Batch. Modeller. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a0198-127">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="a0198-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0198-128">NOTES</span></span>

## <span data-ttu-id="a0198-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0198-129">RELATED LINKS</span></span>

[<span data-ttu-id="a0198-130">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a0198-130">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="a0198-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a0198-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="a0198-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a0198-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="a0198-133">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a0198-133">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="a0198-134">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a0198-134">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="a0198-135">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a0198-135">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


