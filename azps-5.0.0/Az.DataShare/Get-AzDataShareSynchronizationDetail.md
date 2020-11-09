---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
ms.openlocfilehash: 2ee3714895b751223768ac3f98efbd04405ae69f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320325"
---
# <span data-ttu-id="e09c6-101">Get-AzDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="e09c6-101">Get-AzDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="e09c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e09c6-102">SYNOPSIS</span></span>
<span data-ttu-id="e09c6-103">Bir paylaşımın eşitleme ayrıntıları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="e09c6-103">Gets information about synchronization details for a share.</span></span>

## <span data-ttu-id="e09c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e09c6-104">SYNTAX</span></span>

### <span data-ttu-id="e09c6-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e09c6-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationDetail -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e09c6-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e09c6-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e09c6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e09c6-107">DESCRIPTION</span></span>
<span data-ttu-id="e09c6-108">**Get-Azdatasharesynmadizationdetail** cmdlet 'i, bir paylaşım için başlatılan eşitlemenin ayrıntılarını sağlar.</span><span class="sxs-lookup"><span data-stu-id="e09c6-108">The **Get-AzDataShareSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share.</span></span>

## <span data-ttu-id="e09c6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e09c6-109">EXAMPLES</span></span>

### <span data-ttu-id="e09c6-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e09c6-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronizationDetail -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -SynchronizationId "02a17faa-4498-45ee-a884-162180af9251"

DataSetId    : d2411889-5357-4ca8-8d65-9363e46ef2ed
DataSetType  : BlobFolder
EndTime      : 7/8/2019 10:24:27 PM
StartTime    : 7/8/2019 10:23:09 PM
Status       : Succeeded
DurationMs   : 78870
FilesRead    : 1
FilesWritten : 1
SizeRead     : 2779935
SizeWritten  : 2779935
Name         : 16d5161b-2b3f-4d90-b074-13ad7121bcc7
Message      :
```

<span data-ttu-id="e09c6-111">Bu komut, sağlanan eşitleme kimliğine karşılık gelen tüm veri kümelerinin eşitleme ayrıntıları hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="e09c6-111">This command provides information about the synchronization details of all the data sets corresponding to the provided synchronization id.</span></span>

## <span data-ttu-id="e09c6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e09c6-112">PARAMETERS</span></span>

### <span data-ttu-id="e09c6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e09c6-113">-AccountName</span></span>
<span data-ttu-id="e09c6-114">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="e09c6-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e09c6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e09c6-115">-DefaultProfile</span></span>
<span data-ttu-id="e09c6-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e09c6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e09c6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e09c6-117">-ResourceGroupName</span></span>
<span data-ttu-id="e09c6-118">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="e09c6-118">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e09c6-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e09c6-119">-ResourceId</span></span>
<span data-ttu-id="e09c6-120">Azure veri paylaşımı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="e09c6-120">Azure data share resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e09c6-121">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="e09c6-121">-ShareName</span></span>
<span data-ttu-id="e09c6-122">Azure veri paylaşımı adı</span><span class="sxs-lookup"><span data-stu-id="e09c6-122">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e09c6-123">-Synchronizationıd</span><span class="sxs-lookup"><span data-stu-id="e09c6-123">-SynchronizationId</span></span>
<span data-ttu-id="e09c6-124">Paylaşım eşitlemesi kimliği</span><span class="sxs-lookup"><span data-stu-id="e09c6-124">Synchronization id of share synchronization</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e09c6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e09c6-125">CommonParameters</span></span>
<span data-ttu-id="e09c6-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e09c6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e09c6-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e09c6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e09c6-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e09c6-128">INPUTS</span></span>

### <span data-ttu-id="e09c6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e09c6-129">System.String</span></span>

## <span data-ttu-id="e09c6-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e09c6-130">OUTPUTS</span></span>

### <span data-ttu-id="e09c6-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDAtapaylaşım</span><span class="sxs-lookup"><span data-stu-id="e09c6-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="e09c6-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e09c6-132">NOTES</span></span>

## <span data-ttu-id="e09c6-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e09c6-133">RELATED LINKS</span></span>
