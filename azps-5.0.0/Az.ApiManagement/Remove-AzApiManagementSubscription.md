---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 8c6bc7a9e29d6f187285cacdc9df3621fcba8d0f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324022"
---
# <span data-ttu-id="9c7ef-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9c7ef-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="9c7ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c7ef-102">SYNOPSIS</span></span>
<span data-ttu-id="9c7ef-103">Var olan bir aboneliği siler.</span><span class="sxs-lookup"><span data-stu-id="9c7ef-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="9c7ef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9c7ef-104">SYNTAX</span></span>

### <span data-ttu-id="9c7ef-105">ExpandedParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9c7ef-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c7ef-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9c7ef-106">ByInputObject</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -InputObject <PsApiManagementSubscription> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c7ef-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="9c7ef-107">ByResourceId</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9c7ef-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9c7ef-108">DESCRIPTION</span></span>
<span data-ttu-id="9c7ef-109">**Remove-Azapsananagementsubscription** cmdlet 'i var olan bir aboneliği siler.</span><span class="sxs-lookup"><span data-stu-id="9c7ef-109">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="9c7ef-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9c7ef-110">EXAMPLES</span></span>

### <span data-ttu-id="9c7ef-111">Örnek 1: aboneliği silme</span><span class="sxs-lookup"><span data-stu-id="9c7ef-111">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="9c7ef-112">Bu komut, var olan bir aboneliği siler.</span><span class="sxs-lookup"><span data-stu-id="9c7ef-112">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="9c7ef-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9c7ef-113">PARAMETERS</span></span>

### <span data-ttu-id="9c7ef-114">-Context</span><span class="sxs-lookup"><span data-stu-id="9c7ef-114">-Context</span></span>
<span data-ttu-id="9c7ef-115">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c7ef-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c7ef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c7ef-116">-DefaultProfile</span></span>
<span data-ttu-id="9c7ef-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9c7ef-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c7ef-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c7ef-118">-InputObject</span></span>
<span data-ttu-id="9c7ef-119">Psapsananagementsubscription örneği.</span><span class="sxs-lookup"><span data-stu-id="9c7ef-119">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="9c7ef-120">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="9c7ef-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c7ef-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9c7ef-121">-PassThru</span></span>
<span data-ttu-id="9c7ef-122">Bu cmdlet 'in bir $True değerini (başarılı olursa), aksi takdirde $false değerini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c7ef-122">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c7ef-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9c7ef-123">-ResourceId</span></span>
<span data-ttu-id="9c7ef-124">Aboneliğin Kolonu.</span><span class="sxs-lookup"><span data-stu-id="9c7ef-124">Arm ResourceId of Subscription.</span></span> <span data-ttu-id="9c7ef-125">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="9c7ef-125">This parameter is required.</span></span>

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

### <span data-ttu-id="9c7ef-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="9c7ef-126">-SubscriptionId</span></span>
<span data-ttu-id="9c7ef-127">Abonelik KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c7ef-127">Specifies the subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c7ef-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="9c7ef-128">-Confirm</span></span>
<span data-ttu-id="9c7ef-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9c7ef-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c7ef-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c7ef-130">-WhatIf</span></span>
<span data-ttu-id="9c7ef-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9c7ef-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c7ef-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9c7ef-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c7ef-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c7ef-133">CommonParameters</span></span>
<span data-ttu-id="9c7ef-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9c7ef-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c7ef-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9c7ef-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c7ef-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9c7ef-136">INPUTS</span></span>

### <span data-ttu-id="9c7ef-137">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="9c7ef-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9c7ef-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9c7ef-138">System.String</span></span>

### <span data-ttu-id="9c7ef-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9c7ef-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9c7ef-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9c7ef-140">OUTPUTS</span></span>

### <span data-ttu-id="9c7ef-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c7ef-141">System.Boolean</span></span>

## <span data-ttu-id="9c7ef-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9c7ef-142">NOTES</span></span>

## <span data-ttu-id="9c7ef-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9c7ef-143">RELATED LINKS</span></span>

[<span data-ttu-id="9c7ef-144">Get-Azapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="9c7ef-144">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="9c7ef-145">Yeni-Azsız abonelik</span><span class="sxs-lookup"><span data-stu-id="9c7ef-145">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="9c7ef-146">Set-Azapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="9c7ef-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


