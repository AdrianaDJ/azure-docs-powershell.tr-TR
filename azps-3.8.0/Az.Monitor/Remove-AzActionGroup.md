---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
ms.openlocfilehash: 297800cd65f6527a36c8bc486a0ee73e84d98339
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095858"
---
# <span data-ttu-id="eb863-101">Remove-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="eb863-101">Remove-AzActionGroup</span></span>

## <span data-ttu-id="eb863-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb863-102">SYNOPSIS</span></span>
<span data-ttu-id="eb863-103">Eylem grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="eb863-103">Removes an action group.</span></span>

## <span data-ttu-id="eb863-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eb863-104">SYNTAX</span></span>

### <span data-ttu-id="eb863-105">ByPropertyName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="eb863-105">ByPropertyName (Default)</span></span>
```
Remove-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb863-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="eb863-106">ByResourceId</span></span>
```
Remove-AzActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eb863-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="eb863-107">ByInputObject</span></span>
```
Remove-AzActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb863-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="eb863-108">DESCRIPTION</span></span>
<span data-ttu-id="eb863-109">**Remove-AzActionGroup** cmdlet 'i bir eylem grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="eb863-109">The **Remove-AzActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="eb863-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eb863-110">EXAMPLES</span></span>

### <span data-ttu-id="eb863-111">Örnek 1: Eylem grubunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="eb863-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="eb863-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eb863-112">PARAMETERS</span></span>

### <span data-ttu-id="eb863-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb863-113">-DefaultProfile</span></span>
<span data-ttu-id="eb863-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="eb863-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb863-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb863-115">-InputObject</span></span>
<span data-ttu-id="eb863-116">Eylem grubu kaynağı</span><span class="sxs-lookup"><span data-stu-id="eb863-116">The action group resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb863-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="eb863-117">-Name</span></span>
<span data-ttu-id="eb863-118">Eylem grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="eb863-118">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb863-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb863-119">-ResourceGroupName</span></span>
<span data-ttu-id="eb863-120">Kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="eb863-120">The resource group nam</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb863-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="eb863-121">-ResourceId</span></span>
<span data-ttu-id="eb863-122">Kaynak ı</span><span class="sxs-lookup"><span data-stu-id="eb863-122">The resource i</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb863-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="eb863-123">-Confirm</span></span>
<span data-ttu-id="eb863-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eb863-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb863-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb863-125">-WhatIf</span></span>
<span data-ttu-id="eb863-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eb863-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb863-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eb863-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb863-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb863-128">CommonParameters</span></span>
<span data-ttu-id="eb863-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eb863-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb863-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="eb863-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb863-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eb863-131">INPUTS</span></span>

### <span data-ttu-id="eb863-132">System. String</span><span class="sxs-lookup"><span data-stu-id="eb863-132">System.String</span></span>

### <span data-ttu-id="eb863-133">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="eb863-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="eb863-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eb863-134">OUTPUTS</span></span>

### <span data-ttu-id="eb863-135">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="eb863-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="eb863-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eb863-136">NOTES</span></span>

## <span data-ttu-id="eb863-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eb863-137">RELATED LINKS</span></span>

<span data-ttu-id="eb863-138">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Yeni-Azactiongroupahize](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="eb863-138">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
