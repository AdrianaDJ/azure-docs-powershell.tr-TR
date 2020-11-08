---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/save-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 3995506c302d2993623f12fcb7e6e2b9f96fd208
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097606"
---
# <span data-ttu-id="a3ac6-101">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3ac6-101">Save-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="a3ac6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3ac6-102">SYNOPSIS</span></span>
<span data-ttu-id="a3ac6-103">Geçerli yapılandırma için bir işleme oluşturarak değişiklikleri kaydeder.</span><span class="sxs-lookup"><span data-stu-id="a3ac6-103">Saves changes by creating a commit for current configuration.</span></span>

## <span data-ttu-id="a3ac6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a3ac6-104">SYNTAX</span></span>

```
Save-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3ac6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3ac6-105">DESCRIPTION</span></span>
<span data-ttu-id="a3ac6-106">**Save-AzApiManagementTenantGitConfiguration** cmdlet 'i, geçerli yapılandırma anlık görüntüsünü depodaki bir dalda içeren bir kayıt oluşturarak değişiklikleri kaydeder.</span><span class="sxs-lookup"><span data-stu-id="a3ac6-106">The **Save-AzApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="a3ac6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a3ac6-107">EXAMPLES</span></span>

### <span data-ttu-id="a3ac6-108">Örnek 1: değişiklikleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="a3ac6-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="a3ac6-109">Bu komut, geçerli yapılandırma anlık görüntüsüyle depoda belirtilen dalda bir işlem oluşturarak değişiklikleri kaydeder.</span><span class="sxs-lookup"><span data-stu-id="a3ac6-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="a3ac6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a3ac6-110">PARAMETERS</span></span>

### <span data-ttu-id="a3ac6-111">-Dal</span><span class="sxs-lookup"><span data-stu-id="a3ac6-111">-Branch</span></span>
<span data-ttu-id="a3ac6-112">Geçerli yapılandırma anlık görüntüsünün kaydedilmesi gereken git dalının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3ac6-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="a3ac6-113">-Context</span><span class="sxs-lookup"><span data-stu-id="a3ac6-113">-Context</span></span>
<span data-ttu-id="a3ac6-114">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3ac6-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a3ac6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3ac6-115">-DefaultProfile</span></span>
<span data-ttu-id="a3ac6-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a3ac6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3ac6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a3ac6-117">-Force</span></span>
<span data-ttu-id="a3ac6-118">Bu cmdlet 'in geçerli yapılandırma veritabanını git deposuna, git deposunda üzerine yazılmış daha yeni değişiklikler olsa da, geçerli yapılandırma veritabanını bu şekilde işlemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3ac6-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="a3ac6-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a3ac6-119">-PassThru</span></span>
<span data-ttu-id="a3ac6-120">Bu cmdlet 'in **Psapimanagementoperationresult** nesnesini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3ac6-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="a3ac6-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="a3ac6-121">-Confirm</span></span>
<span data-ttu-id="a3ac6-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a3ac6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3ac6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3ac6-123">-WhatIf</span></span>
<span data-ttu-id="a3ac6-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a3ac6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3ac6-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a3ac6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3ac6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3ac6-126">CommonParameters</span></span>
<span data-ttu-id="a3ac6-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a3ac6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3ac6-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a3ac6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3ac6-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a3ac6-129">INPUTS</span></span>

### <span data-ttu-id="a3ac6-130">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="a3ac6-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a3ac6-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a3ac6-131">System.String</span></span>

### <span data-ttu-id="a3ac6-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a3ac6-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a3ac6-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a3ac6-133">OUTPUTS</span></span>

### <span data-ttu-id="a3ac6-134">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementoperationresult</span><span class="sxs-lookup"><span data-stu-id="a3ac6-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="a3ac6-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a3ac6-135">NOTES</span></span>

## <span data-ttu-id="a3ac6-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a3ac6-136">RELATED LINKS</span></span>

[<span data-ttu-id="a3ac6-137">Yayımla-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3ac6-137">Publish-AzApiManagementTenantGitConfiguration</span></span>](./Publish-AzApiManagementTenantGitConfiguration.md)

