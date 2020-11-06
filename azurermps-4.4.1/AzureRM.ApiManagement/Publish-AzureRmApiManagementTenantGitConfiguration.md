---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 2a867109bf44cd652eaf1d256d963796e06762cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588016"
---
# <span data-ttu-id="94d13-101">Publish-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="94d13-101">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="94d13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94d13-102">SYNOPSIS</span></span>
<span data-ttu-id="94d13-103">Bir git dalından yapılandırma veritabanına değişiklikleri yayımlar.</span><span class="sxs-lookup"><span data-stu-id="94d13-103">Publishes changes from a Git branch to the configuration database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94d13-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="94d13-104">SYNTAX</span></span>

```
Publish-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94d13-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="94d13-105">DESCRIPTION</span></span>
<span data-ttu-id="94d13-106">**Publish-AzureRmApiManagementTenantGitConfiguration** cmdlet 'ı bir git dalından yapılandırma veritabanına değişiklikleri yayımlar.</span><span class="sxs-lookup"><span data-stu-id="94d13-106">The **Publish-AzureRmApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="94d13-107">Alternatif olarak, bir git dalındaki değişiklikleri yayımlamadan doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="94d13-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="94d13-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="94d13-108">EXAMPLES</span></span>

### <span data-ttu-id="94d13-109">Örnek 1: git değişikliklerini dağıtma</span><span class="sxs-lookup"><span data-stu-id="94d13-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $ApimContext -Branch 'master' -PassThru
```

<span data-ttu-id="94d13-110">Bu komut, değişiklikleri belirtilen daldan yapılandırma veritabanına yayımlar.</span><span class="sxs-lookup"><span data-stu-id="94d13-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="94d13-111">Örnek 2: git değişikliklerini doğrulama</span><span class="sxs-lookup"><span data-stu-id="94d13-111">Example 2: Validate Git changes</span></span>
```
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $ApimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="94d13-112">Bu komut, git dalındaki değişiklikleri yapılandırma veritabanıyla karşılaştırarak doğrular.</span><span class="sxs-lookup"><span data-stu-id="94d13-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="94d13-113">Değişiklikleri yayımlamaz.</span><span class="sxs-lookup"><span data-stu-id="94d13-113">It does not publish changes.</span></span>

## <span data-ttu-id="94d13-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="94d13-114">PARAMETERS</span></span>

### <span data-ttu-id="94d13-115">-Dal</span><span class="sxs-lookup"><span data-stu-id="94d13-115">-Branch</span></span>
<span data-ttu-id="94d13-116">Bu cmdlet 'in yapılandırmayı yapılandırma veritabanına dağıttığı git dalının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94d13-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

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

### <span data-ttu-id="94d13-117">-Context</span><span class="sxs-lookup"><span data-stu-id="94d13-117">-Context</span></span>
<span data-ttu-id="94d13-118">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="94d13-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="94d13-119">-Force</span><span class="sxs-lookup"><span data-stu-id="94d13-119">-Force</span></span>
<span data-ttu-id="94d13-120">Bu cmdlet 'in bu güncelleştirmede silinen ürünlere yönelik abonelikleri sildiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="94d13-120">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

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

### <span data-ttu-id="94d13-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="94d13-121">-PassThru</span></span>
<span data-ttu-id="94d13-122">Bu cmdlet 'in **Psapimanagementoperationresult** nesnesini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="94d13-122">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="94d13-123">-Yalnızca Validate</span><span class="sxs-lookup"><span data-stu-id="94d13-123">-ValidateOnly</span></span>
<span data-ttu-id="94d13-124">Bu cmdlet 'in belirtilen git dalındaki değişiklikleri doğrulayacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="94d13-124">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="94d13-125">Yapılandırma veritabanında yayımlamaz.</span><span class="sxs-lookup"><span data-stu-id="94d13-125">It does not publish to the configuration database.</span></span>

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

### <span data-ttu-id="94d13-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="94d13-126">-Confirm</span></span>
<span data-ttu-id="94d13-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="94d13-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94d13-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94d13-128">-WhatIf</span></span>
<span data-ttu-id="94d13-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="94d13-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94d13-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="94d13-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94d13-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94d13-131">-DefaultProfile</span></span>
<span data-ttu-id="94d13-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="94d13-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94d13-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94d13-133">CommonParameters</span></span>
<span data-ttu-id="94d13-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="94d13-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94d13-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94d13-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94d13-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="94d13-136">INPUTS</span></span>

## <span data-ttu-id="94d13-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="94d13-137">OUTPUTS</span></span>

### <span data-ttu-id="94d13-138">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementoperationresult</span><span class="sxs-lookup"><span data-stu-id="94d13-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="94d13-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="94d13-139">NOTES</span></span>

## <span data-ttu-id="94d13-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="94d13-140">RELATED LINKS</span></span>

[<span data-ttu-id="94d13-141">Save-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="94d13-141">Save-AzureRmApiManagementTenantGitConfiguration</span></span>](./Save-AzureRmApiManagementTenantGitConfiguration.md)


