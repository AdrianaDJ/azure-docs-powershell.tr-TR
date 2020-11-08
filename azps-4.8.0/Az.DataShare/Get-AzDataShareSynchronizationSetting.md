---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 183164c3f2a18e68b9eab3f505f382a161abf415
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268292"
---
# <span data-ttu-id="2a12e-101">Get-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="2a12e-101">Get-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="2a12e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a12e-102">SYNOPSIS</span></span>
<span data-ttu-id="2a12e-103">Paylaşımda eşitleme ayarı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="2a12e-103">Gets information about synchronization setting on a share.</span></span>

## <span data-ttu-id="2a12e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2a12e-104">SYNTAX</span></span>

### <span data-ttu-id="2a12e-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2a12e-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a12e-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="2a12e-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2a12e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2a12e-107">DESCRIPTION</span></span>
<span data-ttu-id="2a12e-108">**Get-Azdatasharesynmadizationsetting** cmdlet 'i, paylaşımda eşitleme hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="2a12e-108">The **Get-AzDataShareSynchronizationSetting** cmdlet provides information about synchronization enabled on a share.</span></span> 

## <span data-ttu-id="2a12e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2a12e-109">EXAMPLES</span></span>

### <span data-ttu-id="2a12e-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2a12e-110">Example 1</span></span>
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

<span data-ttu-id="2a12e-111">Bu komut, veri paylaşımı hesap WikiAds altındaki Share AdsShare paylaşımında, eşitleme paylaşımı</span><span class="sxs-lookup"><span data-stu-id="2a12e-111">This command provides information about synchronization ShareSynchronization enabled on share AdsShare under data share account WikiAds.</span></span>

## <span data-ttu-id="2a12e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2a12e-112">PARAMETERS</span></span>

### <span data-ttu-id="2a12e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2a12e-113">-AccountName</span></span>
<span data-ttu-id="2a12e-114">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="2a12e-114">Azure data share account name</span></span>

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

### <span data-ttu-id="2a12e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a12e-115">-DefaultProfile</span></span>
<span data-ttu-id="2a12e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2a12e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a12e-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="2a12e-117">-Name</span></span>
<span data-ttu-id="2a12e-118">Eşitleme ayarı adı</span><span class="sxs-lookup"><span data-stu-id="2a12e-118">Name for Synchronization Setting</span></span>

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

### <span data-ttu-id="2a12e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a12e-119">-ResourceGroupName</span></span>
<span data-ttu-id="2a12e-120">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="2a12e-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="2a12e-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2a12e-121">-ResourceId</span></span>
<span data-ttu-id="2a12e-122">Azure veri paylaşımı eşitleme ayarının kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="2a12e-122">The resource id of the azure data share synchronization setting</span></span>

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

### <span data-ttu-id="2a12e-123">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="2a12e-123">-ShareName</span></span>
<span data-ttu-id="2a12e-124">Azure veri paylaşımı adı</span><span class="sxs-lookup"><span data-stu-id="2a12e-124">Azure data share name</span></span>

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

### <span data-ttu-id="2a12e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a12e-125">CommonParameters</span></span>
<span data-ttu-id="2a12e-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2a12e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a12e-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2a12e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a12e-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2a12e-128">INPUTS</span></span>

### <span data-ttu-id="2a12e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2a12e-129">System.String</span></span>

## <span data-ttu-id="2a12e-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2a12e-130">OUTPUTS</span></span>

### <span data-ttu-id="2a12e-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSData</span><span class="sxs-lookup"><span data-stu-id="2a12e-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="2a12e-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2a12e-132">NOTES</span></span>

## <span data-ttu-id="2a12e-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2a12e-133">RELATED LINKS</span></span>
