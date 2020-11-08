---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 5b905083668392ce026bfa416252eb1371ebb640
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097067"
---
# <span data-ttu-id="829d3-101">Get-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="829d3-101">Get-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="829d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="829d3-102">SYNOPSIS</span></span>
<span data-ttu-id="829d3-103">Bir abonelikteki yapılandırılmış güvenlik çalışma alanı ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="829d3-103">Gets the configured security workspace settings on a subscription.</span></span>

## <span data-ttu-id="829d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="829d3-104">SYNTAX</span></span>

### <span data-ttu-id="829d3-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="829d3-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityWorkspaceSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="829d3-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="829d3-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityWorkspaceSetting -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="829d3-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="829d3-107">ResourceId</span></span>
```
Get-AzSecurityWorkspaceSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="829d3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="829d3-108">DESCRIPTION</span></span>
<span data-ttu-id="829d3-109">Bu cmdlet, bu aboneliğin içindeki VM 'lerde yüklü güvenlik Aracısı tarafından toplanan güvenlik verilerini içerecek yapılandırılmış çalışma alanını keşfetmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="829d3-109">This cmdlet lets you discover the configured workspace that will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="829d3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="829d3-110">EXAMPLES</span></span>

### <span data-ttu-id="829d3-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="829d3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityWorkspaceSetting

Id                                                                                                         Name    WorkspaceId                                                                                                                               
--                                                                                                         ----    -----------                                                                                                                               
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityus...
```

<span data-ttu-id="829d3-112">Aboneliğin çalışma alanı ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="829d3-112">Gets the workspace settings for a subscription.</span></span>

## <span data-ttu-id="829d3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="829d3-113">PARAMETERS</span></span>

### <span data-ttu-id="829d3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="829d3-114">-DefaultProfile</span></span>
<span data-ttu-id="829d3-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="829d3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="829d3-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="829d3-116">-Name</span></span>
<span data-ttu-id="829d3-117">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="829d3-117">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="829d3-118">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="829d3-118">-ResourceId</span></span>
<span data-ttu-id="829d3-119">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="829d3-119">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="829d3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="829d3-120">CommonParameters</span></span>
<span data-ttu-id="829d3-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="829d3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="829d3-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="829d3-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="829d3-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="829d3-123">INPUTS</span></span>

### <span data-ttu-id="829d3-124">System. String</span><span class="sxs-lookup"><span data-stu-id="829d3-124">System.String</span></span>

## <span data-ttu-id="829d3-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="829d3-125">OUTPUTS</span></span>

### <span data-ttu-id="829d3-126">Microsoft. Azure. Commands. Security. model.</span><span class="sxs-lookup"><span data-stu-id="829d3-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="829d3-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="829d3-127">NOTES</span></span>

## <span data-ttu-id="829d3-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="829d3-128">RELATED LINKS</span></span>
