---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
ms.openlocfilehash: aa21ea0719c36e5b737b478657e0734eb21a3c3f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108862"
---
# <span data-ttu-id="75e09-101">Set-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="75e09-101">Set-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="75e09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75e09-102">SYNOPSIS</span></span>
<span data-ttu-id="75e09-103">Uygulama ağ geçidine atanan bir kimliği güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="75e09-103">Updates a identity assigned to the application gateway.</span></span>

## <span data-ttu-id="75e09-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="75e09-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75e09-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="75e09-105">DESCRIPTION</span></span>
<span data-ttu-id="75e09-106">**Set-Azapplicationgatewayıdentity** cmdlet 'i, uygulama ağ geçidine atanan bir kimliği güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="75e09-106">The **Set-AzApplicationGatewayIdentity** cmdlet updates an identity assigned to application gateway.</span></span>

## <span data-ttu-id="75e09-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="75e09-107">EXAMPLES</span></span>

### <span data-ttu-id="75e09-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="75e09-108">Example 1</span></span>
```powershell
PS C:\>$appgw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$appgwIdentity = Set-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id -ApplicationGateway $appgw
PS C:\>$updatedAppGw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="75e09-109">Bu örnekte, varolan bir uygulama ağ geçidine Kullanıcı tarafından atanmış bir kimlik atadık.</span><span class="sxs-lookup"><span data-stu-id="75e09-109">In this example, we assign a user assigned identity to an existing application gateway.</span></span>
<span data-ttu-id="75e09-110">Not: bu kimliğin, sertifika/parolaların başvurduğu tuş kasasına erişimi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="75e09-110">Note: This identity should have access to the keyvault from which the certificates/secrets will be referenced.</span></span>

## <span data-ttu-id="75e09-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="75e09-111">PARAMETERS</span></span>

### <span data-ttu-id="75e09-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75e09-112">-ApplicationGateway</span></span>
<span data-ttu-id="75e09-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75e09-113">The applicationGateway</span></span>

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

### <span data-ttu-id="75e09-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75e09-114">-DefaultProfile</span></span>
<span data-ttu-id="75e09-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="75e09-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75e09-116">-Useratandidentityıd</span><span class="sxs-lookup"><span data-stu-id="75e09-116">-UserAssignedIdentityId</span></span>
<span data-ttu-id="75e09-117">Uygulama ağ geçidine atanacak Kullanıcı tarafından atanan kimliğin RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="75e09-117">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="75e09-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="75e09-118">-Confirm</span></span>
<span data-ttu-id="75e09-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="75e09-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75e09-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75e09-120">-WhatIf</span></span>
<span data-ttu-id="75e09-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="75e09-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75e09-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="75e09-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75e09-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75e09-123">CommonParameters</span></span>
<span data-ttu-id="75e09-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="75e09-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75e09-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75e09-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75e09-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="75e09-126">INPUTS</span></span>

### <span data-ttu-id="75e09-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75e09-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="75e09-128">System. String</span><span class="sxs-lookup"><span data-stu-id="75e09-128">System.String</span></span>

## <span data-ttu-id="75e09-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="75e09-129">OUTPUTS</span></span>

### <span data-ttu-id="75e09-130">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75e09-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="75e09-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="75e09-131">NOTES</span></span>

## <span data-ttu-id="75e09-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="75e09-132">RELATED LINKS</span></span>
