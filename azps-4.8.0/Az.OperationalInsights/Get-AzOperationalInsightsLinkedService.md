---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 14f1f96dd533492aedd1c4ed187e380c021a1b5f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268440"
---
# <span data-ttu-id="5b976-101">Get-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="5b976-101">Get-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="5b976-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b976-102">SYNOPSIS</span></span>
<span data-ttu-id="5b976-103">Çalışma alanı için bağlantılı hizmeti alma veya listeleme</span><span class="sxs-lookup"><span data-stu-id="5b976-103">Get or list linked service for workspace</span></span>

## <span data-ttu-id="5b976-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5b976-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b976-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5b976-105">DESCRIPTION</span></span>
<span data-ttu-id="5b976-106">Çalışma alanı için bağlantılı hizmeti alma veya listeleme, "-LinkedServiceName" sağlayıcısı sağlanmadı</span><span class="sxs-lookup"><span data-stu-id="5b976-106">Get or list linked service for workspace, list when "-LinkedServiceName" was not provided</span></span>

## <span data-ttu-id="5b976-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5b976-107">EXAMPLES</span></span>

### <span data-ttu-id="5b976-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5b976-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

Id                    : /subscriptions/{subscription}/resourcegroups/{rg-name}/providers/microsoft.operationalinsights/workspaces/{workspace-name}/linkedservices/cluster
Name                  : {cluster-name}/Cluster
Type                  : Microsoft.OperationalInsights/workspaces/linkedServices
ResourceId            :
WriteAccessResourceId : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
ProvisioningState     : ProvisioningAccount
Tags                  :
```

<span data-ttu-id="5b976-109">Çalışma alanı için bağlantılı hizmeti alma</span><span class="sxs-lookup"><span data-stu-id="5b976-109">Get linked service for workspace</span></span>

## <span data-ttu-id="5b976-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5b976-110">PARAMETERS</span></span>

### <span data-ttu-id="5b976-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b976-111">-DefaultProfile</span></span>
<span data-ttu-id="5b976-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5b976-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b976-113">-Linkedhizmetadı</span><span class="sxs-lookup"><span data-stu-id="5b976-113">-LinkedServiceName</span></span>
<span data-ttu-id="5b976-114">Bağlantılı hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="5b976-114">The linked service name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b976-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b976-115">-ResourceGroupName</span></span>
<span data-ttu-id="5b976-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="5b976-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b976-117">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="5b976-117">-WorkspaceName</span></span>
<span data-ttu-id="5b976-118">Çalışma alanı adı.</span><span class="sxs-lookup"><span data-stu-id="5b976-118">The workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b976-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b976-119">CommonParameters</span></span>
<span data-ttu-id="5b976-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5b976-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b976-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5b976-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b976-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5b976-122">INPUTS</span></span>

### <span data-ttu-id="5b976-123">System. String</span><span class="sxs-lookup"><span data-stu-id="5b976-123">System.String</span></span>

## <span data-ttu-id="5b976-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5b976-124">OUTPUTS</span></span>

### <span data-ttu-id="5b976-125">Microsoft. Azure. Commands. Operationalınsights. model. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="5b976-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="5b976-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5b976-126">NOTES</span></span>

## <span data-ttu-id="5b976-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5b976-127">RELATED LINKS</span></span>
