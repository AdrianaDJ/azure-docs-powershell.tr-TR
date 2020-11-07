---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
ms.openlocfilehash: 72273a95447f9ab0b10460952bc4b26312b9efdb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759097"
---
# <span data-ttu-id="d42e1-101">Get-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="d42e1-101">Get-AzSignalRKey</span></span>

## <span data-ttu-id="d42e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d42e1-102">SYNOPSIS</span></span>
<span data-ttu-id="d42e1-103">Bir SignalR hizmetinin erişim tuşlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="d42e1-103">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="d42e1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d42e1-104">SYNTAX</span></span>

### <span data-ttu-id="d42e1-105">ResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d42e1-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d42e1-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="d42e1-106">ResourceIdParameterSet</span></span>
```
Get-AzSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d42e1-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="d42e1-107">InputObjectParameterSet</span></span>
```
Get-AzSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d42e1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d42e1-108">DESCRIPTION</span></span>
<span data-ttu-id="d42e1-109">Bir SignalR hizmetinin erişim tuşlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="d42e1-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="d42e1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d42e1-110">EXAMPLES</span></span>

### <span data-ttu-id="d42e1-111">Belirli bir SignalR hizmetinin erişim anahtarlarını alma</span><span class="sxs-lookup"><span data-stu-id="d42e1-111">Get access keys of a specific SignalR service</span></span>
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

### <span data-ttu-id="d42e1-112">Yöneltme 'de bir SignalR hizmet nesnesinden erişim tuşları alma</span><span class="sxs-lookup"><span data-stu-id="d42e1-112">Get access keys from a SignalR service object in pipe</span></span>

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

## <span data-ttu-id="d42e1-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d42e1-113">PARAMETERS</span></span>

### <span data-ttu-id="d42e1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d42e1-114">-DefaultProfile</span></span>
<span data-ttu-id="d42e1-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d42e1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d42e1-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d42e1-116">-InputObject</span></span>
<span data-ttu-id="d42e1-117">SignalR kaynak nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d42e1-117">The SignalR resource object.</span></span>

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

### <span data-ttu-id="d42e1-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="d42e1-118">-Name</span></span>
<span data-ttu-id="d42e1-119">SignalR hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="d42e1-119">SignalR service name.</span></span>

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

### <span data-ttu-id="d42e1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d42e1-120">-ResourceGroupName</span></span>
<span data-ttu-id="d42e1-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d42e1-121">Resource group name.</span></span>

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

### <span data-ttu-id="d42e1-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d42e1-122">-ResourceId</span></span>
<span data-ttu-id="d42e1-123">SignalR hizmeti kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d42e1-123">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="d42e1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d42e1-124">CommonParameters</span></span>
<span data-ttu-id="d42e1-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d42e1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d42e1-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d42e1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d42e1-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d42e1-127">INPUTS</span></span>

### <span data-ttu-id="d42e1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d42e1-128">System.String</span></span>

### <span data-ttu-id="d42e1-129">Microsoft. Azure. Commands. SignalR. modeller. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="d42e1-129">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="d42e1-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d42e1-130">OUTPUTS</span></span>

### <span data-ttu-id="d42e1-131">Microsoft. Azure. Commands. SignalR. modeller. PSSignalRKeys</span><span class="sxs-lookup"><span data-stu-id="d42e1-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>

## <span data-ttu-id="d42e1-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d42e1-132">NOTES</span></span>

## <span data-ttu-id="d42e1-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d42e1-133">RELATED LINKS</span></span>
