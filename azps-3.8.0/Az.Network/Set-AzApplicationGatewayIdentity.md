---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
ms.openlocfilehash: aa21ea0719c36e5b737b478657e0734eb21a3c3f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096825"
---
# <span data-ttu-id="f3327-101">Set-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="f3327-101">Set-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="f3327-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3327-102">SYNOPSIS</span></span>
<span data-ttu-id="f3327-103">Uygulama ağ geçidine atanan bir kimliği güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f3327-103">Updates a identity assigned to the application gateway.</span></span>

## <span data-ttu-id="f3327-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f3327-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3327-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f3327-105">DESCRIPTION</span></span>
<span data-ttu-id="f3327-106">**Set-Azapplicationgatewayıdentity** cmdlet 'i, uygulama ağ geçidine atanan bir kimliği güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f3327-106">The **Set-AzApplicationGatewayIdentity** cmdlet updates an identity assigned to application gateway.</span></span>

## <span data-ttu-id="f3327-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f3327-107">EXAMPLES</span></span>

### <span data-ttu-id="f3327-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f3327-108">Example 1</span></span>
```powershell
PS C:\>$appgw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$appgwIdentity = Set-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id -ApplicationGateway $appgw
PS C:\>$updatedAppGw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="f3327-109">Bu örnekte, varolan bir uygulama ağ geçidine Kullanıcı tarafından atanmış bir kimlik atadık.</span><span class="sxs-lookup"><span data-stu-id="f3327-109">In this example, we assign a user assigned identity to an existing application gateway.</span></span>
<span data-ttu-id="f3327-110">Not: bu kimliğin, sertifika/parolaların başvurduğu tuş kasasına erişimi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f3327-110">Note: This identity should have access to the keyvault from which the certificates/secrets will be referenced.</span></span>

## <span data-ttu-id="f3327-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f3327-111">PARAMETERS</span></span>

### <span data-ttu-id="f3327-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f3327-112">-ApplicationGateway</span></span>
<span data-ttu-id="f3327-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f3327-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3327-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3327-114">-DefaultProfile</span></span>
<span data-ttu-id="f3327-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f3327-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3327-116">-Useratandidentityıd</span><span class="sxs-lookup"><span data-stu-id="f3327-116">-UserAssignedIdentityId</span></span>
<span data-ttu-id="f3327-117">Uygulama ağ geçidine atanacak Kullanıcı tarafından atanan kimliğin RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="f3327-117">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: UserAssignedIdentity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3327-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="f3327-118">-Confirm</span></span>
<span data-ttu-id="f3327-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f3327-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3327-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3327-120">-WhatIf</span></span>
<span data-ttu-id="f3327-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f3327-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3327-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f3327-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3327-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3327-123">CommonParameters</span></span>
<span data-ttu-id="f3327-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f3327-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3327-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3327-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3327-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f3327-126">INPUTS</span></span>

### <span data-ttu-id="f3327-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f3327-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="f3327-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f3327-128">System.String</span></span>

## <span data-ttu-id="f3327-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f3327-129">OUTPUTS</span></span>

### <span data-ttu-id="f3327-130">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f3327-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f3327-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f3327-131">NOTES</span></span>

## <span data-ttu-id="f3327-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f3327-132">RELATED LINKS</span></span>