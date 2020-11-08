---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
ms.openlocfilehash: efdcab51a8dfa6d886a317fa1707b65861cf2563
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104140"
---
# <span data-ttu-id="9c993-101">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="9c993-101">Get-AzBatchApplication</span></span>

## <span data-ttu-id="9c993-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c993-102">SYNOPSIS</span></span>
<span data-ttu-id="9c993-103">Belirtilen uygulama hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="9c993-103">Gets information about the specified application.</span></span>

## <span data-ttu-id="9c993-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9c993-104">SYNTAX</span></span>

```
Get-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c993-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9c993-105">DESCRIPTION</span></span>
<span data-ttu-id="9c993-106">**Get-AzBatchApplication** cmdlet 'ı bir Azure toplu hesabındaki bir uygulamayla ilgili bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="9c993-106">The **Get-AzBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="9c993-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9c993-107">EXAMPLES</span></span>

### <span data-ttu-id="9c993-108">Örnek 1: uygulamaları bir toplu Iş hesabında görüntüleme</span><span class="sxs-lookup"><span data-stu-id="9c993-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationName AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="9c993-109">Bu komut, ContosoBatch hesabındaki tüm uygulamaları görüntüler.</span><span class="sxs-lookup"><span data-stu-id="9c993-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="9c993-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9c993-110">PARAMETERS</span></span>

### <span data-ttu-id="9c993-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9c993-111">-AccountName</span></span>
<span data-ttu-id="9c993-112">Uygulamayı içeren toplu Iş hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c993-112">Specifies the name of the Batch account that contains the application.</span></span>

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

### <span data-ttu-id="9c993-113">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="9c993-113">-ApplicationName</span></span>
<span data-ttu-id="9c993-114">Uygulamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c993-114">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c993-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c993-115">-DefaultProfile</span></span>
<span data-ttu-id="9c993-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9c993-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c993-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c993-117">-ResourceGroupName</span></span>
<span data-ttu-id="9c993-118">Toplu Iş hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c993-118">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="9c993-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c993-119">CommonParameters</span></span>
<span data-ttu-id="9c993-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9c993-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c993-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9c993-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c993-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9c993-122">INPUTS</span></span>

### <span data-ttu-id="9c993-123">System. String</span><span class="sxs-lookup"><span data-stu-id="9c993-123">System.String</span></span>

## <span data-ttu-id="9c993-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9c993-124">OUTPUTS</span></span>

### <span data-ttu-id="9c993-125">Microsoft.Azure.Commands.Batch. Modeller. PSApplication</span><span class="sxs-lookup"><span data-stu-id="9c993-125">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="9c993-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9c993-126">NOTES</span></span>

## <span data-ttu-id="9c993-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9c993-127">RELATED LINKS</span></span>

[<span data-ttu-id="9c993-128">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="9c993-128">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="9c993-129">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="9c993-129">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="9c993-130">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="9c993-130">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="9c993-131">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="9c993-131">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="9c993-132">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="9c993-132">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="9c993-133">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="9c993-133">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


