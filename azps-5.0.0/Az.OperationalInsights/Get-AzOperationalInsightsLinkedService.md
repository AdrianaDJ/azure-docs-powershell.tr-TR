---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 14f1f96dd533492aedd1c4ed187e380c021a1b5f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277576"
---
# <span data-ttu-id="15955-101">Get-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="15955-101">Get-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="15955-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15955-102">SYNOPSIS</span></span>
<span data-ttu-id="15955-103">Çalışma alanı için bağlantılı hizmeti alma veya listeleme</span><span class="sxs-lookup"><span data-stu-id="15955-103">Get or list linked service for workspace</span></span>

## <span data-ttu-id="15955-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15955-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15955-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="15955-105">DESCRIPTION</span></span>
<span data-ttu-id="15955-106">Çalışma alanı için bağlantılı hizmeti alma veya listeleme, "-LinkedServiceName" sağlayıcısı sağlanmadı</span><span class="sxs-lookup"><span data-stu-id="15955-106">Get or list linked service for workspace, list when "-LinkedServiceName" was not provided</span></span>

## <span data-ttu-id="15955-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15955-107">EXAMPLES</span></span>

### <span data-ttu-id="15955-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="15955-108">Example 1</span></span>
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

<span data-ttu-id="15955-109">Çalışma alanı için bağlantılı hizmeti alma</span><span class="sxs-lookup"><span data-stu-id="15955-109">Get linked service for workspace</span></span>

## <span data-ttu-id="15955-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15955-110">PARAMETERS</span></span>

### <span data-ttu-id="15955-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15955-111">-DefaultProfile</span></span>
<span data-ttu-id="15955-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="15955-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15955-113">-Linkedhizmetadı</span><span class="sxs-lookup"><span data-stu-id="15955-113">-LinkedServiceName</span></span>
<span data-ttu-id="15955-114">Bağlantılı hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="15955-114">The linked service name.</span></span>

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

### <span data-ttu-id="15955-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15955-115">-ResourceGroupName</span></span>
<span data-ttu-id="15955-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="15955-116">The resource group name.</span></span>

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

### <span data-ttu-id="15955-117">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="15955-117">-WorkspaceName</span></span>
<span data-ttu-id="15955-118">Çalışma alanı adı.</span><span class="sxs-lookup"><span data-stu-id="15955-118">The workspace name.</span></span>

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

### <span data-ttu-id="15955-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15955-119">CommonParameters</span></span>
<span data-ttu-id="15955-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15955-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15955-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="15955-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15955-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15955-122">INPUTS</span></span>

### <span data-ttu-id="15955-123">System. String</span><span class="sxs-lookup"><span data-stu-id="15955-123">System.String</span></span>

## <span data-ttu-id="15955-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15955-124">OUTPUTS</span></span>

### <span data-ttu-id="15955-125">Microsoft. Azure. Commands. Operationalınsights. model. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="15955-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="15955-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15955-126">NOTES</span></span>

## <span data-ttu-id="15955-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15955-127">RELATED LINKS</span></span>
