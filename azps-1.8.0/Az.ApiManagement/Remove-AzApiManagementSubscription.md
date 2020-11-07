---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 411fa67d81b772c2e9dcd6b1690e8eac50de3ea0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917744"
---
# <span data-ttu-id="099ae-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="099ae-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="099ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="099ae-102">SYNOPSIS</span></span>
<span data-ttu-id="099ae-103">Var olan bir aboneliği siler.</span><span class="sxs-lookup"><span data-stu-id="099ae-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="099ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="099ae-104">SYNTAX</span></span>

```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="099ae-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="099ae-105">DESCRIPTION</span></span>
<span data-ttu-id="099ae-106">**Remove-Azapsananagementsubscription** cmdlet 'i var olan bir aboneliği siler.</span><span class="sxs-lookup"><span data-stu-id="099ae-106">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="099ae-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="099ae-107">EXAMPLES</span></span>

### <span data-ttu-id="099ae-108">Örnek 1: aboneliği silme</span><span class="sxs-lookup"><span data-stu-id="099ae-108">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="099ae-109">Bu komut, var olan bir aboneliği siler.</span><span class="sxs-lookup"><span data-stu-id="099ae-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="099ae-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="099ae-110">PARAMETERS</span></span>

### <span data-ttu-id="099ae-111">-Context</span><span class="sxs-lookup"><span data-stu-id="099ae-111">-Context</span></span>
<span data-ttu-id="099ae-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="099ae-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="099ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="099ae-113">-DefaultProfile</span></span>
<span data-ttu-id="099ae-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="099ae-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="099ae-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="099ae-115">-PassThru</span></span>
<span data-ttu-id="099ae-116">Bu cmdlet 'in bir $True değerini (başarılı olursa), aksi takdirde $false değerini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="099ae-116">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="099ae-117">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="099ae-117">-SubscriptionId</span></span>
<span data-ttu-id="099ae-118">Abonelik KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="099ae-118">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="099ae-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="099ae-119">-Confirm</span></span>
<span data-ttu-id="099ae-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="099ae-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="099ae-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="099ae-121">-WhatIf</span></span>
<span data-ttu-id="099ae-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="099ae-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="099ae-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="099ae-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="099ae-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="099ae-124">CommonParameters</span></span>
<span data-ttu-id="099ae-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="099ae-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="099ae-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="099ae-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="099ae-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="099ae-127">INPUTS</span></span>

### <span data-ttu-id="099ae-128">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="099ae-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="099ae-129">System. String</span><span class="sxs-lookup"><span data-stu-id="099ae-129">System.String</span></span>

### <span data-ttu-id="099ae-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="099ae-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="099ae-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="099ae-131">OUTPUTS</span></span>

### <span data-ttu-id="099ae-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="099ae-132">System.Boolean</span></span>

## <span data-ttu-id="099ae-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="099ae-133">NOTES</span></span>

## <span data-ttu-id="099ae-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="099ae-134">RELATED LINKS</span></span>

[<span data-ttu-id="099ae-135">Get-Azapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="099ae-135">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="099ae-136">Yeni-Azsız abonelik</span><span class="sxs-lookup"><span data-stu-id="099ae-136">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="099ae-137">Set-Azapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="099ae-137">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


