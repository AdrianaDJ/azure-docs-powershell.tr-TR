---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzExternalSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzExternalSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzExternalSecuritySolution.md
ms.openlocfilehash: 0314a7e6b661b0b007ffe2cf59f5618247e4b282
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107644"
---
# <span data-ttu-id="85071-101">Get-AzExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="85071-101">Get-AzExternalSecuritySolution</span></span>

## <span data-ttu-id="85071-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85071-102">SYNOPSIS</span></span>
<span data-ttu-id="85071-103">Dış güvenlik çözümünü alma</span><span class="sxs-lookup"><span data-stu-id="85071-103">Get external security solution</span></span> 

## <span data-ttu-id="85071-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="85071-104">SYNTAX</span></span>

### <span data-ttu-id="85071-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="85071-105">SubscriptionScope (Default)</span></span>
```
Get-AzExternalSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85071-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="85071-106">ResourceGroupLevelResource</span></span>
```
Get-AzExternalSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85071-107">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="85071-107">SubscriptionLevelResource</span></span>
```
Get-AzExternalSecuritySolution -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="85071-108">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="85071-108">ResourceId</span></span>
```
Get-AzExternalSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85071-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="85071-109">DESCRIPTION</span></span>
<span data-ttu-id="85071-110">Dış güvenlik çözümünü alma</span><span class="sxs-lookup"><span data-stu-id="85071-110">Get external security solution</span></span>

## <span data-ttu-id="85071-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="85071-111">EXAMPLES</span></span>

### <span data-ttu-id="85071-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="85071-112">Example 1</span></span>
```powershell
PS C:\> Get-AzExternalSecuritySolution
ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/defaultresourcegroup-eus/provide
                    rs/microsoft.operationalinsights/workspaces/defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-e
                    us
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/defaultresourcegroup-eus/provide
                    rs/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_defaultworkspace-487bb485-b
                    5b0-471e-9c0d-10717612f869-eus
Name              : aad_defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-eus
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/defaultresourcegroup-weu/provide
                    rs/microsoft.operationalinsights/workspaces/defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-w
                    eu
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/defaultresourcegroup-weu/provide
                    rs/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_defaultworkspace-487bb485-b
                    5b0-471e-9c0d-10717612f869-weu
Name              : aad_defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-weu
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.opera
                    tionalinsights/workspaces/securityuserws
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/mainws/providers/Microsoft.Secur
                    ity/locations/centralus/externalSecuritySolutions/aad_securityuserws
Name              : aad_securityuserws
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/myservice1/providers/microsoft.o
                    perationalinsights/workspaces/testservicews
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myservice1/providers/Microsoft.S
                    ecurity/locations/centralus/externalSecuritySolutions/aad_testservicews
Name              : aad_testservicews
Kind              : AAD
```

<span data-ttu-id="85071-113">Abonelikteki tüm dış güvenlik çözümlerini alma</span><span class="sxs-lookup"><span data-stu-id="85071-113">Get all the external security solutions in the subscription</span></span>

### <span data-ttu-id="85071-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="85071-114">Example 2</span></span>
```powershell
PS C:\> Get-AzExternalSecuritySolution -ResourceGroupName "myservice1" -Location "centralus" -Name "aad_testservicews"
ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/myservice1/providers/microsoft.operationalinsights/workspaces/testservicews
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myservice1/providers/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_testservicews
Name              : aad_testservicews
Kind              : AAD
```

<span data-ttu-id="85071-115">Belirli bir dış güvenlik çözümünü edinme</span><span class="sxs-lookup"><span data-stu-id="85071-115">Get a specific external security solution</span></span>

## <span data-ttu-id="85071-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="85071-116">PARAMETERS</span></span>

### <span data-ttu-id="85071-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85071-117">-DefaultProfile</span></span>
<span data-ttu-id="85071-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="85071-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85071-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="85071-119">-Location</span></span>
<span data-ttu-id="85071-120">Konumuyla.</span><span class="sxs-lookup"><span data-stu-id="85071-120">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85071-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="85071-121">-Name</span></span>
<span data-ttu-id="85071-122">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="85071-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85071-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85071-123">-ResourceGroupName</span></span>
<span data-ttu-id="85071-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="85071-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85071-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="85071-125">-ResourceId</span></span>
<span data-ttu-id="85071-126">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="85071-126">Resource ID.</span></span>

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

### <span data-ttu-id="85071-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85071-127">CommonParameters</span></span>
<span data-ttu-id="85071-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="85071-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85071-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="85071-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85071-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="85071-130">INPUTS</span></span>

### <span data-ttu-id="85071-131">System. String</span><span class="sxs-lookup"><span data-stu-id="85071-131">System.String</span></span>

## <span data-ttu-id="85071-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="85071-132">OUTPUTS</span></span>

### <span data-ttu-id="85071-133">Microsoft. Azure. Commands. Security. model. ExternalSecuritySolutions. PSSecurityExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="85071-133">Microsoft.Azure.Commands.Security.Models.ExternalSecuritySolutions.PSSecurityExternalSecuritySolution</span></span>

## <span data-ttu-id="85071-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="85071-134">NOTES</span></span>

## <span data-ttu-id="85071-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="85071-135">RELATED LINKS</span></span>
