---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
ms.openlocfilehash: b3bb193b47acf0f77851e5b9f4549d455a568b15
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276287"
---
# <span data-ttu-id="f598e-101">Get-AzSmartGroup</span><span class="sxs-lookup"><span data-stu-id="f598e-101">Get-AzSmartGroup</span></span>

## <span data-ttu-id="f598e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f598e-102">SYNOPSIS</span></span>
<span data-ttu-id="f598e-103">Akıllı grup bilgilerini alır</span><span class="sxs-lookup"><span data-stu-id="f598e-103">Gets Smart Groups information</span></span>

## <span data-ttu-id="f598e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f598e-104">SYNTAX</span></span>

### <span data-ttu-id="f598e-105">SmartGroupsListByFilter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f598e-105">SmartGroupsListByFilter (Default)</span></span>
```
Get-AzSmartGroup [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f598e-106">Smartgroupbyıd</span><span class="sxs-lookup"><span data-stu-id="f598e-106">SmartGroupById</span></span>
```
Get-AzSmartGroup -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f598e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f598e-107">DESCRIPTION</span></span>
<span data-ttu-id="f598e-108">**Get-AzSmartGroup** cmdlet 'i akıllı gruplar bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="f598e-108">**Get-AzSmartGroup** cmdlet gets smart groups information.</span></span>

## <span data-ttu-id="f598e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f598e-109">EXAMPLES</span></span>

### <span data-ttu-id="f598e-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f598e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroup -TimeRange "1h"
```

<span data-ttu-id="f598e-111">Son 1 saat içinde oluşturulmuş tüm akıllı grupları listeler.</span><span class="sxs-lookup"><span data-stu-id="f598e-111">List all smart groups formed in last 1 hour.</span></span> <span data-ttu-id="f598e-112">Listedeki her bir akıllı grubun ayrıntılarını almak için Format-List kullanın.</span><span class="sxs-lookup"><span data-stu-id="f598e-112">Use Format-List to get the complete details of each smart group in list.</span></span>

### <span data-ttu-id="f598e-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f598e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSmartGroup -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="f598e-114">Kimlik (GUID) veya kaynak kimliği (tam ARM kimliği) ile akıllı Grup ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="f598e-114">Get Smart Group details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="f598e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f598e-115">PARAMETERS</span></span>

### <span data-ttu-id="f598e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f598e-116">-DefaultProfile</span></span>
<span data-ttu-id="f598e-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f598e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f598e-118">-Smartgroupıd</span><span class="sxs-lookup"><span data-stu-id="f598e-118">-SmartGroupId</span></span>
<span data-ttu-id="f598e-119">Smartgroup 'un smartgroup/RESOURCEID benzersiz tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="f598e-119">Unique Identifier of SmartGroup / ResourceId of SmartGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f598e-120">-Sıralaölçüt</span><span class="sxs-lookup"><span data-stu-id="f598e-120">-SortBy</span></span>
<span data-ttu-id="f598e-121">Sıralama sırasında kullanılacak uyarı özelliği</span><span class="sxs-lookup"><span data-stu-id="f598e-121">Alert property to use while sorting</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f598e-122">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="f598e-122">-SortOrder</span></span>
<span data-ttu-id="f598e-123">Sıralama düzeni</span><span class="sxs-lookup"><span data-stu-id="f598e-123">Sort Order</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f598e-124">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="f598e-124">-TimeRange</span></span>
<span data-ttu-id="f598e-125">Desteklenen zaman aralığı değerleri-1h, 1G, 7d, 30D (varsayılan olarak 1G)</span><span class="sxs-lookup"><span data-stu-id="f598e-125">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f598e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f598e-126">CommonParameters</span></span>
<span data-ttu-id="f598e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f598e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f598e-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f598e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f598e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f598e-129">INPUTS</span></span>

### <span data-ttu-id="f598e-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f598e-130">None</span></span>

## <span data-ttu-id="f598e-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f598e-131">OUTPUTS</span></span>

### <span data-ttu-id="f598e-132">Microsoft. Azure. Commands. AlertsManagement. Outputmodel. PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="f598e-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="f598e-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f598e-133">NOTES</span></span>

## <span data-ttu-id="f598e-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f598e-134">RELATED LINKS</span></span>
