---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/save-azurermapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 9b297771f05b35493f8a852fd6d3450d2b5e7531
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763504"
---
# <span data-ttu-id="c7e5e-101">Save-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7e5e-101">Save-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="c7e5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7e5e-102">SYNOPSIS</span></span>
<span data-ttu-id="c7e5e-103">Geçerli yapılandırma için bir işleme oluşturarak değişiklikleri kaydeder.</span><span class="sxs-lookup"><span data-stu-id="c7e5e-103">Saves changes by creating a commit for current configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7e5e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c7e5e-104">SYNTAX</span></span>

```
Save-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7e5e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c7e5e-105">DESCRIPTION</span></span>
<span data-ttu-id="c7e5e-106">**Save-AzureRmApiManagementTenantGitConfiguration** cmdlet 'i, geçerli yapılandırma anlık görüntüsünü depodaki bir dalda içeren bir kayıt oluşturarak değişiklikleri kaydeder.</span><span class="sxs-lookup"><span data-stu-id="c7e5e-106">The **Save-AzureRmApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="c7e5e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c7e5e-107">EXAMPLES</span></span>

### <span data-ttu-id="c7e5e-108">Örnek 1: değişiklikleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="c7e5e-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzureRmApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="c7e5e-109">Bu komut, geçerli yapılandırma anlık görüntüsüyle depoda belirtilen dalda bir işlem oluşturarak değişiklikleri kaydeder.</span><span class="sxs-lookup"><span data-stu-id="c7e5e-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="c7e5e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c7e5e-110">PARAMETERS</span></span>

### <span data-ttu-id="c7e5e-111">-Dal</span><span class="sxs-lookup"><span data-stu-id="c7e5e-111">-Branch</span></span>
<span data-ttu-id="c7e5e-112">Geçerli yapılandırma anlık görüntüsünün kaydedilmesi gereken git dalının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7e5e-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="c7e5e-113">-Context</span><span class="sxs-lookup"><span data-stu-id="c7e5e-113">-Context</span></span>
<span data-ttu-id="c7e5e-114">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7e5e-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c7e5e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7e5e-115">-DefaultProfile</span></span>
<span data-ttu-id="c7e5e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c7e5e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7e5e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c7e5e-117">-Force</span></span>
<span data-ttu-id="c7e5e-118">Bu cmdlet 'in geçerli yapılandırma veritabanını git deposuna, git deposunda üzerine yazılmış daha yeni değişiklikler olsa da, geçerli yapılandırma veritabanını bu şekilde işlemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7e5e-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="c7e5e-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c7e5e-119">-PassThru</span></span>
<span data-ttu-id="c7e5e-120">Bu cmdlet 'in **Psapimanagementoperationresult** nesnesini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7e5e-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="c7e5e-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="c7e5e-121">-Confirm</span></span>
<span data-ttu-id="c7e5e-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c7e5e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7e5e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7e5e-123">-WhatIf</span></span>
<span data-ttu-id="c7e5e-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c7e5e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7e5e-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c7e5e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7e5e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7e5e-126">CommonParameters</span></span>
<span data-ttu-id="c7e5e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c7e5e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7e5e-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7e5e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7e5e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c7e5e-129">INPUTS</span></span>

### <span data-ttu-id="c7e5e-130">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="c7e5e-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c7e5e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c7e5e-131">System.String</span></span>

### <span data-ttu-id="c7e5e-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c7e5e-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c7e5e-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c7e5e-133">OUTPUTS</span></span>

### <span data-ttu-id="c7e5e-134">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementoperationresult</span><span class="sxs-lookup"><span data-stu-id="c7e5e-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="c7e5e-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c7e5e-135">NOTES</span></span>

## <span data-ttu-id="c7e5e-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c7e5e-136">RELATED LINKS</span></span>

[<span data-ttu-id="c7e5e-137">Yayımla-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7e5e-137">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>](./Publish-AzureRmApiManagementTenantGitConfiguration.md)


