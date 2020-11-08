---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
ms.openlocfilehash: 8e0f62f4b3d29d0aff9a2bdfcd7916805544af14
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937867"
---
# <span data-ttu-id="01580-101">Get-AzDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="01580-101">Get-AzDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="01580-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01580-102">SYNOPSIS</span></span>
<span data-ttu-id="01580-103">Bir paylaşımın eşitleme ayrıntıları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="01580-103">Gets information about synchronization details for a share.</span></span>

## <span data-ttu-id="01580-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="01580-104">SYNTAX</span></span>

### <span data-ttu-id="01580-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="01580-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationDetail -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01580-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="01580-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01580-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="01580-107">DESCRIPTION</span></span>
<span data-ttu-id="01580-108">**Get-Azdatasharesynmadizationdetail** cmdlet 'i, bir paylaşım için başlatılan eşitlemenin ayrıntılarını sağlar.</span><span class="sxs-lookup"><span data-stu-id="01580-108">The **Get-AzDataShareSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share.</span></span>

## <span data-ttu-id="01580-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="01580-109">EXAMPLES</span></span>

### <span data-ttu-id="01580-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="01580-110">Example 1</span></span>
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

<span data-ttu-id="01580-111">Bu komut, sağlanan eşitleme kimliğine karşılık gelen tüm veri kümelerinin eşitleme ayrıntıları hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="01580-111">This command provides information about the synchronization details of all the data sets corresponding to the provided synchronization id.</span></span>

## <span data-ttu-id="01580-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="01580-112">PARAMETERS</span></span>

### <span data-ttu-id="01580-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="01580-113">-AccountName</span></span>
<span data-ttu-id="01580-114">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="01580-114">Azure data share account name</span></span>

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

### <span data-ttu-id="01580-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01580-115">-DefaultProfile</span></span>
<span data-ttu-id="01580-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="01580-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01580-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01580-117">-ResourceGroupName</span></span>
<span data-ttu-id="01580-118">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="01580-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="01580-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="01580-119">-ResourceId</span></span>
<span data-ttu-id="01580-120">Azure veri paylaşımı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="01580-120">Azure data share resource id</span></span>

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

### <span data-ttu-id="01580-121">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="01580-121">-ShareName</span></span>
<span data-ttu-id="01580-122">Azure veri paylaşımı adı</span><span class="sxs-lookup"><span data-stu-id="01580-122">Azure data share name</span></span>

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

### <span data-ttu-id="01580-123">-Synchronizationıd</span><span class="sxs-lookup"><span data-stu-id="01580-123">-SynchronizationId</span></span>
<span data-ttu-id="01580-124">Paylaşım eşitlemesi kimliği</span><span class="sxs-lookup"><span data-stu-id="01580-124">Synchronization id of share synchronization</span></span>

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

### <span data-ttu-id="01580-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01580-125">CommonParameters</span></span>
<span data-ttu-id="01580-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="01580-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01580-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01580-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01580-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="01580-128">INPUTS</span></span>

### <span data-ttu-id="01580-129">System. String</span><span class="sxs-lookup"><span data-stu-id="01580-129">System.String</span></span>

## <span data-ttu-id="01580-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="01580-130">OUTPUTS</span></span>

### <span data-ttu-id="01580-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDAtapaylaşım</span><span class="sxs-lookup"><span data-stu-id="01580-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="01580-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="01580-132">NOTES</span></span>

## <span data-ttu-id="01580-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="01580-133">RELATED LINKS</span></span>