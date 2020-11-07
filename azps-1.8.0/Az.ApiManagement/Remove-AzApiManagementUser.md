---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
ms.openlocfilehash: c8c4a318f3d2e972e742afcbdc13350a0ff77a90
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917740"
---
# <span data-ttu-id="f2e98-101">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f2e98-101">Remove-AzApiManagementUser</span></span>

## <span data-ttu-id="f2e98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2e98-102">SYNOPSIS</span></span>
<span data-ttu-id="f2e98-103">Var olan kullanıcıyı siler.</span><span class="sxs-lookup"><span data-stu-id="f2e98-103">Deletes an existing user.</span></span>

## <span data-ttu-id="f2e98-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f2e98-104">SYNTAX</span></span>

```
Remove-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2e98-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f2e98-105">DESCRIPTION</span></span>
<span data-ttu-id="f2e98-106">**Remove-Azapsananagementuser** cmdlet 'i var olan kullanıcıyı siler.</span><span class="sxs-lookup"><span data-stu-id="f2e98-106">The **Remove-AzApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="f2e98-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f2e98-107">EXAMPLES</span></span>

### <span data-ttu-id="f2e98-108">Örnek 1: Kullanıcı silme</span><span class="sxs-lookup"><span data-stu-id="f2e98-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="f2e98-109">Bu komut mevcut bir kullanıcıyı siler.</span><span class="sxs-lookup"><span data-stu-id="f2e98-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="f2e98-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f2e98-110">PARAMETERS</span></span>

### <span data-ttu-id="f2e98-111">-Context</span><span class="sxs-lookup"><span data-stu-id="f2e98-111">-Context</span></span>
<span data-ttu-id="f2e98-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2e98-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="f2e98-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="f2e98-113">This parameter is required.</span></span>

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

### <span data-ttu-id="f2e98-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2e98-114">-DefaultProfile</span></span>
<span data-ttu-id="f2e98-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f2e98-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2e98-116">-Deleteabonelikleri</span><span class="sxs-lookup"><span data-stu-id="f2e98-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="f2e98-117">Ürüne aboneliklerin silineceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2e98-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="f2e98-118">Bu parametre belirtilmemişse ve bir abonelik varsa, bu cmdlet bir istisna oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f2e98-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="f2e98-119">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="f2e98-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="f2e98-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f2e98-120">-PassThru</span></span>
<span data-ttu-id="f2e98-121">Bu cmdlet 'in bir $Ture değerini (başarılı olursa), aksi takdirde $False değerini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2e98-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="f2e98-122">-UserID</span><span class="sxs-lookup"><span data-stu-id="f2e98-122">-UserId</span></span>
<span data-ttu-id="f2e98-123">Kaldırılacak kullanıcının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2e98-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="f2e98-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="f2e98-124">-Confirm</span></span>
<span data-ttu-id="f2e98-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f2e98-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2e98-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2e98-126">-WhatIf</span></span>
<span data-ttu-id="f2e98-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f2e98-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2e98-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f2e98-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2e98-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2e98-129">CommonParameters</span></span>
<span data-ttu-id="f2e98-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f2e98-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2e98-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2e98-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2e98-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f2e98-132">INPUTS</span></span>

### <span data-ttu-id="f2e98-133">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="f2e98-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f2e98-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f2e98-134">System.String</span></span>

### <span data-ttu-id="f2e98-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f2e98-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f2e98-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f2e98-136">OUTPUTS</span></span>

### <span data-ttu-id="f2e98-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f2e98-137">System.Boolean</span></span>

## <span data-ttu-id="f2e98-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f2e98-138">NOTES</span></span>

## <span data-ttu-id="f2e98-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f2e98-139">RELATED LINKS</span></span>

[<span data-ttu-id="f2e98-140">Get-Azsız Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="f2e98-140">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="f2e98-141">Yeni-Azsız Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="f2e98-141">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="f2e98-142">Set-Azapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="f2e98-142">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)

