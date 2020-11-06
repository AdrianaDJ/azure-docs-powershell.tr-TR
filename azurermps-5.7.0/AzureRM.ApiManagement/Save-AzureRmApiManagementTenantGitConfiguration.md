---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/save-azurermapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 7401c359a9af82d1b65749a3276aada89ab9320d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586833"
---
# <span data-ttu-id="812e2-101">Save-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="812e2-101">Save-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="812e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="812e2-102">SYNOPSIS</span></span>
<span data-ttu-id="812e2-103">Geçerli yapılandırma için bir işleme oluşturarak değişiklikleri kaydeder.</span><span class="sxs-lookup"><span data-stu-id="812e2-103">Saves changes by creating a commit for current configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="812e2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="812e2-104">SYNTAX</span></span>

```
Save-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="812e2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="812e2-105">DESCRIPTION</span></span>
<span data-ttu-id="812e2-106">**Save-AzureRmApiManagementTenantGitConfiguration** cmdlet 'i, geçerli yapılandırma anlık görüntüsünü depodaki bir dalda içeren bir kayıt oluşturarak değişiklikleri kaydeder.</span><span class="sxs-lookup"><span data-stu-id="812e2-106">The **Save-AzureRmApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="812e2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="812e2-107">EXAMPLES</span></span>

### <span data-ttu-id="812e2-108">Örnek 1: değişiklikleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="812e2-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzureRmApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="812e2-109">Bu komut, geçerli yapılandırma anlık görüntüsüyle depoda belirtilen dalda bir işlem oluşturarak değişiklikleri kaydeder.</span><span class="sxs-lookup"><span data-stu-id="812e2-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="812e2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="812e2-110">PARAMETERS</span></span>

### <span data-ttu-id="812e2-111">-Dal</span><span class="sxs-lookup"><span data-stu-id="812e2-111">-Branch</span></span>
<span data-ttu-id="812e2-112">Geçerli yapılandırma anlık görüntüsünün kaydedilmesi gereken git dalının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="812e2-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="812e2-113">-Context</span><span class="sxs-lookup"><span data-stu-id="812e2-113">-Context</span></span>
<span data-ttu-id="812e2-114">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="812e2-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="812e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="812e2-115">-DefaultProfile</span></span>
<span data-ttu-id="812e2-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="812e2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="812e2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="812e2-117">-Force</span></span>
<span data-ttu-id="812e2-118">Bu cmdlet 'in geçerli yapılandırma veritabanını git deposuna, git deposunda üzerine yazılmış daha yeni değişiklikler olsa da, geçerli yapılandırma veritabanını bu şekilde işlemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="812e2-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="812e2-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="812e2-119">-PassThru</span></span>
<span data-ttu-id="812e2-120">Bu cmdlet 'in **Psapimanagementoperationresult** nesnesini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="812e2-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="812e2-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="812e2-121">-Confirm</span></span>
<span data-ttu-id="812e2-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="812e2-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="812e2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="812e2-123">-WhatIf</span></span>
<span data-ttu-id="812e2-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="812e2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="812e2-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="812e2-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="812e2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="812e2-126">CommonParameters</span></span>
<span data-ttu-id="812e2-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="812e2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="812e2-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="812e2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="812e2-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="812e2-129">INPUTS</span></span>

### <span data-ttu-id="812e2-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="812e2-130">None</span></span>
<span data-ttu-id="812e2-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="812e2-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="812e2-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="812e2-132">OUTPUTS</span></span>

### <span data-ttu-id="812e2-133">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementoperationresult</span><span class="sxs-lookup"><span data-stu-id="812e2-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="812e2-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="812e2-134">NOTES</span></span>

## <span data-ttu-id="812e2-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="812e2-135">RELATED LINKS</span></span>

[<span data-ttu-id="812e2-136">Yayımla-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="812e2-136">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>](./Publish-AzureRmApiManagementTenantGitConfiguration.md)


