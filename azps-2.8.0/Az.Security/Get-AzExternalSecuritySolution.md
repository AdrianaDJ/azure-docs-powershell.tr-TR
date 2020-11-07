---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzExternalSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzExternalSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzExternalSecuritySolution.md
ms.openlocfilehash: cf06d1cce2e37f69ce06576a659dbfa989ca56b9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932512"
---
# <span data-ttu-id="3e98e-101">Get-AzExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="3e98e-101">Get-AzExternalSecuritySolution</span></span>

## <span data-ttu-id="3e98e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e98e-102">SYNOPSIS</span></span>
<span data-ttu-id="3e98e-103">Dış güvenlik çözümünü alma</span><span class="sxs-lookup"><span data-stu-id="3e98e-103">Get external security solution</span></span> 

## <span data-ttu-id="3e98e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3e98e-104">SYNTAX</span></span>

### <span data-ttu-id="3e98e-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3e98e-105">SubscriptionScope (Default)</span></span>
```
Get-AzExternalSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e98e-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="3e98e-106">ResourceGroupLevelResource</span></span>
```
Get-AzExternalSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e98e-107">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="3e98e-107">SubscriptionLevelResource</span></span>
```
Get-AzExternalSecuritySolution -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e98e-108">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="3e98e-108">ResourceId</span></span>
```
Get-AzExternalSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e98e-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="3e98e-109">DESCRIPTION</span></span>
<span data-ttu-id="3e98e-110">Dış güvenlik çözümünü alma</span><span class="sxs-lookup"><span data-stu-id="3e98e-110">Get external security solution</span></span>

## <span data-ttu-id="3e98e-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3e98e-111">EXAMPLES</span></span>

### <span data-ttu-id="3e98e-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3e98e-112">Example 1</span></span>
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

<span data-ttu-id="3e98e-113">Abonelikteki tüm dış güvenlik çözümlerini alma</span><span class="sxs-lookup"><span data-stu-id="3e98e-113">Get all the external security solutions in the subscription</span></span>

### <span data-ttu-id="3e98e-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3e98e-114">Example 2</span></span>
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

<span data-ttu-id="3e98e-115">Belirli bir dış güvenlik çözümünü edinme</span><span class="sxs-lookup"><span data-stu-id="3e98e-115">Get a specific external security solution</span></span>

## <span data-ttu-id="3e98e-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3e98e-116">PARAMETERS</span></span>

### <span data-ttu-id="3e98e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e98e-117">-DefaultProfile</span></span>
<span data-ttu-id="3e98e-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3e98e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e98e-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="3e98e-119">-Location</span></span>
<span data-ttu-id="3e98e-120">Konumuyla.</span><span class="sxs-lookup"><span data-stu-id="3e98e-120">Location.</span></span>

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

### <span data-ttu-id="3e98e-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="3e98e-121">-Name</span></span>
<span data-ttu-id="3e98e-122">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="3e98e-122">Resource name.</span></span>

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

### <span data-ttu-id="3e98e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e98e-123">-ResourceGroupName</span></span>
<span data-ttu-id="3e98e-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3e98e-124">Resource group name.</span></span>

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

### <span data-ttu-id="3e98e-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3e98e-125">-ResourceId</span></span>
<span data-ttu-id="3e98e-126">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3e98e-126">Resource ID.</span></span>

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

### <span data-ttu-id="3e98e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e98e-127">CommonParameters</span></span>
<span data-ttu-id="3e98e-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3e98e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e98e-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e98e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e98e-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3e98e-130">INPUTS</span></span>

### <span data-ttu-id="3e98e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3e98e-131">System.String</span></span>

## <span data-ttu-id="3e98e-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3e98e-132">OUTPUTS</span></span>

### <span data-ttu-id="3e98e-133">Microsoft. Azure. Commands. Security. model. ExternalSecuritySolutions. PSSecurityExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="3e98e-133">Microsoft.Azure.Commands.Security.Models.ExternalSecuritySolutions.PSSecurityExternalSecuritySolution</span></span>

## <span data-ttu-id="3e98e-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3e98e-134">NOTES</span></span>

## <span data-ttu-id="3e98e-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3e98e-135">RELATED LINKS</span></span>
