---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
ms.openlocfilehash: 0cbcc49f4b37b150b783467f45dcc7d4d7e53f2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753182"
---
# <span data-ttu-id="d3648-101">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d3648-101">Get-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="d3648-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3648-102">SYNOPSIS</span></span>
<span data-ttu-id="d3648-103">Bir toplu Iş hesabındaki uygulama paketi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d3648-103">Gets information about an application package in a Batch account.</span></span>

## <span data-ttu-id="d3648-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3648-104">SYNTAX</span></span>

```
Get-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3648-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3648-105">DESCRIPTION</span></span>
<span data-ttu-id="d3648-106">**Get-AzBatchApplicationPackage** cmdlet 'i, bir Azure toplu hesabındaki uygulama paketi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d3648-106">The **Get-AzBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="d3648-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3648-107">EXAMPLES</span></span>

### <span data-ttu-id="d3648-108">Örnek 1: bir toplu Iş hesabındaki uygulama paketinin ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="d3648-108">Example 1: Get details of an application package in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0"
Format             : zip
State              : Active
Version            : 1.0
LastActivationTime : 13/05/2016 4:03:24 AM
StorageUrl         : https://contosobatch.blob.core.windows.net/app-test
StorageUrlExpiry   : 13/05/2016 8:04:44 AM
Id                 : litware
```

<span data-ttu-id="d3648-109">Bu komut, Litwin paketinin 1,0 sürümündeki ayrıntıları alır.</span><span class="sxs-lookup"><span data-stu-id="d3648-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="d3648-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3648-110">PARAMETERS</span></span>

### <span data-ttu-id="d3648-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d3648-111">-AccountName</span></span>
<span data-ttu-id="d3648-112">Bu cmdlet 'in bilgi aldığı toplu Iş hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3648-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="d3648-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d3648-113">-ApplicationId</span></span>
<span data-ttu-id="d3648-114">Uygulamanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3648-114">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="d3648-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="d3648-115">-ApplicationVersion</span></span>
<span data-ttu-id="d3648-116">Uygulamanın sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3648-116">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="d3648-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3648-117">-DefaultProfile</span></span>
<span data-ttu-id="d3648-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d3648-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3648-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3648-119">-ResourceGroupName</span></span>
<span data-ttu-id="d3648-120">Toplu Iş hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3648-120">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="d3648-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3648-121">CommonParameters</span></span>
<span data-ttu-id="d3648-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3648-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3648-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3648-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3648-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3648-124">INPUTS</span></span>

### <span data-ttu-id="d3648-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d3648-125">System.String</span></span>

## <span data-ttu-id="d3648-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3648-126">OUTPUTS</span></span>

### <span data-ttu-id="d3648-127">Microsoft.Azure.Commands.Batch. Modeller. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d3648-127">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="d3648-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3648-128">NOTES</span></span>

## <span data-ttu-id="d3648-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3648-129">RELATED LINKS</span></span>

[<span data-ttu-id="d3648-130">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d3648-130">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="d3648-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d3648-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="d3648-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d3648-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="d3648-133">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d3648-133">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="d3648-134">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d3648-134">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="d3648-135">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d3648-135">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


