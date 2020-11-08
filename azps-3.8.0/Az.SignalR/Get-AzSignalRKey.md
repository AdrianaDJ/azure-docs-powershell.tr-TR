---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
ms.openlocfilehash: e71795c04d421ad0c6772ddd23724b5d53d38e86
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096267"
---
# <span data-ttu-id="c62df-101">Get-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="c62df-101">Get-AzSignalRKey</span></span>

## <span data-ttu-id="c62df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c62df-102">SYNOPSIS</span></span>
<span data-ttu-id="c62df-103">Bir SignalR hizmetinin erişim tuşlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="c62df-103">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="c62df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c62df-104">SYNTAX</span></span>

### <span data-ttu-id="c62df-105">ResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c62df-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c62df-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c62df-106">ResourceIdParameterSet</span></span>
```
Get-AzSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c62df-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="c62df-107">InputObjectParameterSet</span></span>
```
Get-AzSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c62df-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c62df-108">DESCRIPTION</span></span>
<span data-ttu-id="c62df-109">Bir SignalR hizmetinin erişim tuşlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="c62df-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="c62df-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c62df-110">EXAMPLES</span></span>

### <span data-ttu-id="c62df-111">Belirli bir SignalR hizmetinin erişim anahtarlarını alma</span><span class="sxs-lookup"><span data-stu-id="c62df-111">Get access keys of a specific SignalR service</span></span>
```powershell
PS C:\> Get-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

### <span data-ttu-id="c62df-112">Yöneltme 'de bir SignalR hizmet nesnesinden erişim tuşları alma</span><span class="sxs-lookup"><span data-stu-id="c62df-112">Get access keys from a SignalR service object in pipe</span></span>

```powershell
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 | Get-AzSignalRKey

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

## <span data-ttu-id="c62df-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c62df-113">PARAMETERS</span></span>

### <span data-ttu-id="c62df-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c62df-114">-DefaultProfile</span></span>
<span data-ttu-id="c62df-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c62df-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c62df-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c62df-116">-InputObject</span></span>
<span data-ttu-id="c62df-117">SignalR kaynak nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c62df-117">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c62df-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="c62df-118">-Name</span></span>
<span data-ttu-id="c62df-119">SignalR hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="c62df-119">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c62df-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c62df-120">-ResourceGroupName</span></span>
<span data-ttu-id="c62df-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c62df-121">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c62df-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c62df-122">-ResourceId</span></span>
<span data-ttu-id="c62df-123">SignalR hizmeti kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c62df-123">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c62df-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c62df-124">CommonParameters</span></span>
<span data-ttu-id="c62df-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c62df-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c62df-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c62df-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c62df-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c62df-127">INPUTS</span></span>

### <span data-ttu-id="c62df-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c62df-128">System.String</span></span>
### <span data-ttu-id="c62df-129">Microsoft. Azure. Commands. SignalR. modeller. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="c62df-129">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="c62df-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c62df-130">OUTPUTS</span></span>

### <span data-ttu-id="c62df-131">Microsoft. Azure. Commands. SignalR. modeller. PSSignalRKeys</span><span class="sxs-lookup"><span data-stu-id="c62df-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>
## <span data-ttu-id="c62df-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c62df-132">NOTES</span></span>

## <span data-ttu-id="c62df-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c62df-133">RELATED LINKS</span></span>
