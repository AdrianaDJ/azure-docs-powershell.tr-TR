---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: c071db20f6ed0207b48d7373cd1d485592c30e01
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103845"
---
# <span data-ttu-id="0015b-101">Get-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="0015b-101">Get-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="0015b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0015b-102">SYNOPSIS</span></span>
<span data-ttu-id="0015b-103">Paylaşımda eşitleme ayarı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="0015b-103">Gets information about synchronization setting on a share.</span></span>

## <span data-ttu-id="0015b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0015b-104">SYNTAX</span></span>

### <span data-ttu-id="0015b-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0015b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0015b-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="0015b-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0015b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0015b-107">DESCRIPTION</span></span>
<span data-ttu-id="0015b-108">**Get-Azdatasharesynmadizationsetting** cmdlet 'i, paylaşımda eşitleme hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="0015b-108">The **Get-AzDataShareSynchronizationSetting** cmdlet provides information about synchronization enabled on a share.</span></span> 

## <span data-ttu-id="0015b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0015b-109">EXAMPLES</span></span>

### <span data-ttu-id="0015b-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0015b-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ShareSynchronization"

RecurrenceInterval  : Day
SynchronizationTime : 7/9/2019 9:00:00 AM
ProvisioningState   : Succeeded
CreatedAt           : 7/10/2019 12:01:08 AM
CreatedBy           : ADS Test
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.
                      DataShare/accounts/WikiAds/shares/AdShare/synchronizationSettings/ShareSynchronization
Name                : ShareSynchronization
Type                : Microsoft.DataShare/SynchronizationSettings
```

<span data-ttu-id="0015b-111">Bu komut, veri paylaşımı hesap WikiAds altındaki Share AdsShare paylaşımında, eşitleme paylaşımı</span><span class="sxs-lookup"><span data-stu-id="0015b-111">This command provides information about synchronization ShareSynchronization enabled on share AdsShare under data share account WikiAds.</span></span>

## <span data-ttu-id="0015b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0015b-112">PARAMETERS</span></span>

### <span data-ttu-id="0015b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0015b-113">-AccountName</span></span>
<span data-ttu-id="0015b-114">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="0015b-114">Azure data share account name</span></span>

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

### <span data-ttu-id="0015b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0015b-115">-DefaultProfile</span></span>
<span data-ttu-id="0015b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0015b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0015b-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="0015b-117">-Name</span></span>
<span data-ttu-id="0015b-118">Eşitleme ayarı adı</span><span class="sxs-lookup"><span data-stu-id="0015b-118">Name for Synchronization Setting</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0015b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0015b-119">-ResourceGroupName</span></span>
<span data-ttu-id="0015b-120">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="0015b-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="0015b-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0015b-121">-ResourceId</span></span>
<span data-ttu-id="0015b-122">Azure veri paylaşımı eşitleme ayarının kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="0015b-122">The resource id of the azure data share synchronization setting</span></span>

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

### <span data-ttu-id="0015b-123">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="0015b-123">-ShareName</span></span>
<span data-ttu-id="0015b-124">Azure veri paylaşımı adı</span><span class="sxs-lookup"><span data-stu-id="0015b-124">Azure data share name</span></span>

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

### <span data-ttu-id="0015b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0015b-125">CommonParameters</span></span>
<span data-ttu-id="0015b-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0015b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0015b-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0015b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0015b-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0015b-128">INPUTS</span></span>

### <span data-ttu-id="0015b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0015b-129">System.String</span></span>

## <span data-ttu-id="0015b-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0015b-130">OUTPUTS</span></span>

### <span data-ttu-id="0015b-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSData</span><span class="sxs-lookup"><span data-stu-id="0015b-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="0015b-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0015b-132">NOTES</span></span>

## <span data-ttu-id="0015b-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0015b-133">RELATED LINKS</span></span>
