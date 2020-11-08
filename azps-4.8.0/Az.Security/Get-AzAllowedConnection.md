---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzAllowedConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
ms.openlocfilehash: 3a604cbdda30612016763fef75fcf62e0c8e36f7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108761"
---
# <span data-ttu-id="b2e2e-101">Get-AzAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="b2e2e-101">Get-AzAllowedConnection</span></span>

## <span data-ttu-id="b2e2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2e2e-102">SYNOPSIS</span></span>
<span data-ttu-id="b2e2e-103">Aboneliğin kaynakları arasında izin verilen trafiği görüntülemek için kullanılır</span><span class="sxs-lookup"><span data-stu-id="b2e2e-103">Used to display allowed traffic between resources for the subscription</span></span>


## <span data-ttu-id="b2e2e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b2e2e-104">SYNTAX</span></span>

### <span data-ttu-id="b2e2e-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b2e2e-105">SubscriptionScope (Default)</span></span>
```
Get-AzAllowedConnection [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2e2e-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="b2e2e-106">ResourceGroupLevelResource</span></span>
```
Get-AzAllowedConnection -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2e2e-107">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b2e2e-107">-ResourceId</span></span>
```
Get-AzAllowedConnection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2e2e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b2e2e-108">DESCRIPTION</span></span>
<span data-ttu-id="b2e2e-109">Abonelik ve konum kaynakları arasındaki olası tüm trafiğin listesini, bağlantı türüne göre alır.</span><span class="sxs-lookup"><span data-stu-id="b2e2e-109">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="b2e2e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b2e2e-110">EXAMPLES</span></span>

### <span data-ttu-id="b2e2e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b2e2e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAllowedConnection
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/virtualMachines
Name:   Internal
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

### <span data-ttu-id="b2e2e-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b2e2e-112">Example 2</span></span>
```powershell
PS C:\> Get-AzAllowedConnection -ResourceGroupName "myService1" -Location "centralus" -Name "Internal"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/Internal
Name:   virtualMachines
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="b2e2e-113">Abonelik ve konum kaynakları arasındaki olası tüm trafiğin listesini, bağlantı türüne göre alır.</span><span class="sxs-lookup"><span data-stu-id="b2e2e-113">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="b2e2e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b2e2e-114">PARAMETERS</span></span>

### <span data-ttu-id="b2e2e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2e2e-115">-DefaultProfile</span></span>
<span data-ttu-id="b2e2e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b2e2e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2e2e-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="b2e2e-117">-Location</span></span>
<span data-ttu-id="b2e2e-118">Konumuyla.</span><span class="sxs-lookup"><span data-stu-id="b2e2e-118">Location.</span></span>

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

### <span data-ttu-id="b2e2e-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="b2e2e-119">-Name</span></span>
<span data-ttu-id="b2e2e-120">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="b2e2e-120">Resource name.</span></span>

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

### <span data-ttu-id="b2e2e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2e2e-121">-ResourceGroupName</span></span>
<span data-ttu-id="b2e2e-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b2e2e-122">Resource group name.</span></span>

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

### <span data-ttu-id="b2e2e-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b2e2e-123">-ResourceId</span></span>
<span data-ttu-id="b2e2e-124">Komutu çağırmak istediğiniz güvenlik kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b2e2e-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="b2e2e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2e2e-125">CommonParameters</span></span>
<span data-ttu-id="b2e2e-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b2e2e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2e2e-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2e2e-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2e2e-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b2e2e-128">INPUTS</span></span>

### <span data-ttu-id="b2e2e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b2e2e-129">System.String</span></span>

## <span data-ttu-id="b2e2e-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b2e2e-130">OUTPUTS</span></span>

### <span data-ttu-id="b2e2e-131">Microsoft. Azure. Commands. Security. model. AllowedConnection. Pssecurityallodilimlerin Connection</span><span class="sxs-lookup"><span data-stu-id="b2e2e-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span></span>


## <span data-ttu-id="b2e2e-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b2e2e-132">NOTES</span></span>

## <span data-ttu-id="b2e2e-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b2e2e-133">RELATED LINKS</span></span>
