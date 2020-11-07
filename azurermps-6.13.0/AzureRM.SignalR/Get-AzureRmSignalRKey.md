---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/get-azurermsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalRKey.md
ms.openlocfilehash: 3eaef21cc9652ee7e5e4c52a51bcc3ab8bd5b1c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762714"
---
# <span data-ttu-id="caf34-101">Get-AzureRmSignalRKey</span><span class="sxs-lookup"><span data-stu-id="caf34-101">Get-AzureRmSignalRKey</span></span>

## <span data-ttu-id="caf34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="caf34-102">SYNOPSIS</span></span>
<span data-ttu-id="caf34-103">Bir SignalR hizmetinin erişim tuşlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="caf34-103">Get the access keys of a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="caf34-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="caf34-104">SYNTAX</span></span>

### <span data-ttu-id="caf34-105">ResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="caf34-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="caf34-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="caf34-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="caf34-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="caf34-107">InputObjectParameterSet</span></span>
```
Get-AzureRmSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="caf34-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="caf34-108">DESCRIPTION</span></span>
<span data-ttu-id="caf34-109">Bir SignalR hizmetinin erişim tuşlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="caf34-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="caf34-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="caf34-110">EXAMPLES</span></span>

### <span data-ttu-id="caf34-111">Belirli bir SignalR hizmetinin erişim anahtarlarını alma</span><span class="sxs-lookup"><span data-stu-id="caf34-111">Get access keys of a specific SignalR service</span></span>
```powershell
PS C:\> Get-AzureRmSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

### <span data-ttu-id="caf34-112">Yöneltme 'de bir SignalR hizmet nesnesinden erişim tuşları alma</span><span class="sxs-lookup"><span data-stu-id="caf34-112">Get access keys from a SignalR service object in pipe</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 | Get-AzureRmSignalRKey

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

## <span data-ttu-id="caf34-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="caf34-113">PARAMETERS</span></span>

### <span data-ttu-id="caf34-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caf34-114">-DefaultProfile</span></span>
<span data-ttu-id="caf34-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="caf34-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf34-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="caf34-116">-InputObject</span></span>
<span data-ttu-id="caf34-117">SignalR kaynak nesnesi.</span><span class="sxs-lookup"><span data-stu-id="caf34-117">The SignalR resource object.</span></span>

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

### <span data-ttu-id="caf34-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="caf34-118">-Name</span></span>
<span data-ttu-id="caf34-119">SignalR hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="caf34-119">SignalR service name.</span></span>

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

### <span data-ttu-id="caf34-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="caf34-120">-ResourceGroupName</span></span>
<span data-ttu-id="caf34-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="caf34-121">Resource group name.</span></span>

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

### <span data-ttu-id="caf34-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="caf34-122">-ResourceId</span></span>
<span data-ttu-id="caf34-123">SignalR hizmeti kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="caf34-123">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="caf34-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caf34-124">CommonParameters</span></span>
<span data-ttu-id="caf34-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="caf34-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caf34-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caf34-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caf34-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="caf34-127">INPUTS</span></span>

### <span data-ttu-id="caf34-128">System. String</span><span class="sxs-lookup"><span data-stu-id="caf34-128">System.String</span></span>
<span data-ttu-id="caf34-129">Parametreler: RESOURCEID (ByValue)</span><span class="sxs-lookup"><span data-stu-id="caf34-129">Parameters: ResourceId (ByValue)</span></span>

### <span data-ttu-id="caf34-130">Microsoft. Azure. Commands. SignalR. modeller. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="caf34-130">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
<span data-ttu-id="caf34-131">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="caf34-131">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="caf34-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="caf34-132">OUTPUTS</span></span>

### <span data-ttu-id="caf34-133">Microsoft. Azure. Commands. SignalR. modeller. PSSignalRKeys</span><span class="sxs-lookup"><span data-stu-id="caf34-133">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>

## <span data-ttu-id="caf34-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="caf34-134">NOTES</span></span>

## <span data-ttu-id="caf34-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="caf34-135">RELATED LINKS</span></span>
