---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityWorkspaceSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityWorkspaceSetting.md
ms.openlocfilehash: 7e2a655810c885245d3694fb63caa44c5b4119e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762902"
---
# <span data-ttu-id="36b93-101">Get-AzureRmSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="36b93-101">Get-AzureRmSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="36b93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36b93-102">SYNOPSIS</span></span>
<span data-ttu-id="36b93-103">Bir abonelikteki yapılandırılmış güvenlik çalışma alanı ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="36b93-103">Gets the configured security workspace settings on a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36b93-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="36b93-104">SYNTAX</span></span>

### <span data-ttu-id="36b93-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="36b93-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityWorkspaceSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36b93-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="36b93-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityWorkspaceSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="36b93-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="36b93-107">ResourceId</span></span>
```
Get-AzureRmSecurityWorkspaceSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36b93-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="36b93-108">DESCRIPTION</span></span>
<span data-ttu-id="36b93-109">Bu cmdlet, bu aboneliğin içindeki VM 'lerde yüklü güvenlik Aracısı tarafından toplanan güvenlik verilerini içerecek yapılandırılmış çalışma alanını keşfetmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="36b93-109">This cmdlet lets you discover the configured workspace that will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="36b93-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="36b93-110">EXAMPLES</span></span>

### <span data-ttu-id="36b93-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="36b93-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityWorkspaceSetting

Id                                                                                                         Name    WorkspaceId                                                                                                                               
--                                                                                                         ----    -----------                                                                                                                               
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityus...
```

<span data-ttu-id="36b93-112">Aboneliğin çalışma alanı ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="36b93-112">Gets the workspace settings for a subscription.</span></span>

## <span data-ttu-id="36b93-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="36b93-113">PARAMETERS</span></span>

### <span data-ttu-id="36b93-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36b93-114">-DefaultProfile</span></span>
<span data-ttu-id="36b93-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="36b93-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b93-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="36b93-116">-Name</span></span>
<span data-ttu-id="36b93-117">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="36b93-117">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b93-118">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="36b93-118">-ResourceId</span></span>
<span data-ttu-id="36b93-119">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="36b93-119">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36b93-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36b93-120">CommonParameters</span></span>
<span data-ttu-id="36b93-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="36b93-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36b93-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36b93-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36b93-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="36b93-123">INPUTS</span></span>

### <span data-ttu-id="36b93-124">System. String</span><span class="sxs-lookup"><span data-stu-id="36b93-124">System.String</span></span>

## <span data-ttu-id="36b93-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="36b93-125">OUTPUTS</span></span>

### <span data-ttu-id="36b93-126">Microsoft. Azure. Commands. Security. model.</span><span class="sxs-lookup"><span data-stu-id="36b93-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="36b93-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="36b93-127">NOTES</span></span>

## <span data-ttu-id="36b93-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="36b93-128">RELATED LINKS</span></span>
