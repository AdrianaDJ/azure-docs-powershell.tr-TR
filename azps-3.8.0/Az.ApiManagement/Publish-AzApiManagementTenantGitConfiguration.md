---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/publish-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 288bb02ffad3669615df3535aec7f691162daa2a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097682"
---
# <span data-ttu-id="a9e54-101">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="a9e54-101">Publish-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="a9e54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9e54-102">SYNOPSIS</span></span>
<span data-ttu-id="a9e54-103">Bir git dalından yapılandırma veritabanına değişiklikleri yayımlar.</span><span class="sxs-lookup"><span data-stu-id="a9e54-103">Publishes changes from a Git branch to the configuration database.</span></span>

## <span data-ttu-id="a9e54-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9e54-104">SYNTAX</span></span>

```
Publish-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9e54-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9e54-105">DESCRIPTION</span></span>
<span data-ttu-id="a9e54-106">**Publish-AzApiManagementTenantGitConfiguration** cmdlet 'ı bir git dalından yapılandırma veritabanına değişiklikleri yayımlar.</span><span class="sxs-lookup"><span data-stu-id="a9e54-106">The **Publish-AzApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="a9e54-107">Alternatif olarak, bir git dalındaki değişiklikleri yayımlamadan doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a9e54-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="a9e54-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9e54-108">EXAMPLES</span></span>

### <span data-ttu-id="a9e54-109">Örnek 1: git değişikliklerini dağıtma</span><span class="sxs-lookup"><span data-stu-id="a9e54-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="a9e54-110">Bu komut, değişiklikleri belirtilen daldan yapılandırma veritabanına yayımlar.</span><span class="sxs-lookup"><span data-stu-id="a9e54-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="a9e54-111">Örnek 2: git değişikliklerini doğrulama</span><span class="sxs-lookup"><span data-stu-id="a9e54-111">Example 2: Validate Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="a9e54-112">Bu komut, git dalındaki değişiklikleri yapılandırma veritabanıyla karşılaştırarak doğrular.</span><span class="sxs-lookup"><span data-stu-id="a9e54-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="a9e54-113">Değişiklikleri yayımlamaz.</span><span class="sxs-lookup"><span data-stu-id="a9e54-113">It does not publish changes.</span></span>

## <span data-ttu-id="a9e54-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9e54-114">PARAMETERS</span></span>

### <span data-ttu-id="a9e54-115">-Dal</span><span class="sxs-lookup"><span data-stu-id="a9e54-115">-Branch</span></span>
<span data-ttu-id="a9e54-116">Bu cmdlet 'in yapılandırmayı yapılandırma veritabanına dağıttığı git dalının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9e54-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

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

### <span data-ttu-id="a9e54-117">-Context</span><span class="sxs-lookup"><span data-stu-id="a9e54-117">-Context</span></span>
<span data-ttu-id="a9e54-118">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9e54-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a9e54-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9e54-119">-DefaultProfile</span></span>
<span data-ttu-id="a9e54-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a9e54-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9e54-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a9e54-121">-Force</span></span>
<span data-ttu-id="a9e54-122">Bu cmdlet 'in bu güncelleştirmede silinen ürünlere yönelik abonelikleri sildiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="a9e54-122">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

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

### <span data-ttu-id="a9e54-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a9e54-123">-PassThru</span></span>
<span data-ttu-id="a9e54-124">Bu cmdlet 'in **Psapimanagementoperationresult** nesnesini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9e54-124">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="a9e54-125">-Yalnızca Validate</span><span class="sxs-lookup"><span data-stu-id="a9e54-125">-ValidateOnly</span></span>
<span data-ttu-id="a9e54-126">Bu cmdlet 'in belirtilen git dalındaki değişiklikleri doğrulayacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9e54-126">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="a9e54-127">Yapılandırma veritabanında yayımlamaz.</span><span class="sxs-lookup"><span data-stu-id="a9e54-127">It does not publish to the configuration database.</span></span>

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

### <span data-ttu-id="a9e54-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="a9e54-128">-Confirm</span></span>
<span data-ttu-id="a9e54-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a9e54-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9e54-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9e54-130">-WhatIf</span></span>
<span data-ttu-id="a9e54-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9e54-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9e54-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a9e54-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9e54-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9e54-133">CommonParameters</span></span>
<span data-ttu-id="a9e54-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9e54-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9e54-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a9e54-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9e54-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9e54-136">INPUTS</span></span>

### <span data-ttu-id="a9e54-137">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="a9e54-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a9e54-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a9e54-138">System.String</span></span>

### <span data-ttu-id="a9e54-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a9e54-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a9e54-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9e54-140">OUTPUTS</span></span>

### <span data-ttu-id="a9e54-141">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementoperationresult</span><span class="sxs-lookup"><span data-stu-id="a9e54-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="a9e54-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9e54-142">NOTES</span></span>

## <span data-ttu-id="a9e54-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9e54-143">RELATED LINKS</span></span>

[<span data-ttu-id="a9e54-144">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="a9e54-144">Save-AzApiManagementTenantGitConfiguration</span></span>](./Save-AzApiManagementTenantGitConfiguration.md)

