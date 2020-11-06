---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantSyncState.md
ms.openlocfilehash: c75660c60788d5b2a099be97c927328464f34dba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588658"
---
# <span data-ttu-id="1d0b3-101">Get-AzureRmApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="1d0b3-101">Get-AzureRmApiManagementTenantSyncState</span></span>

## <span data-ttu-id="1d0b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d0b3-102">SYNOPSIS</span></span>
<span data-ttu-id="1d0b3-103">Yapılandırma veritabanıyla git deposu arasındaki en son eşitlemenin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="1d0b3-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d0b3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1d0b3-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantSyncState -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d0b3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1d0b3-105">DESCRIPTION</span></span>
<span data-ttu-id="1d0b3-106">**Get-Azurermapsananagementtenantsyncstate** cmdlet 'i, yapılandırma veritabanı ile git deposu arasındaki en son eşitlemenin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="1d0b3-106">The **Get-AzureRmApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="1d0b3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1d0b3-107">EXAMPLES</span></span>

### <span data-ttu-id="1d0b3-108">Örnek 1: en son eşitlemenin durumunu alma</span><span class="sxs-lookup"><span data-stu-id="1d0b3-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantSyncState -Context $apimContext
```

<span data-ttu-id="1d0b3-109">Bu komut, yapılandırma veritabanıyla git deposu arasındaki en son eşitlemenin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="1d0b3-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="1d0b3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1d0b3-110">PARAMETERS</span></span>

### <span data-ttu-id="1d0b3-111">-Context</span><span class="sxs-lookup"><span data-stu-id="1d0b3-111">-Context</span></span>
<span data-ttu-id="1d0b3-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d0b3-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1d0b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d0b3-113">-DefaultProfile</span></span>
<span data-ttu-id="1d0b3-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1d0b3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d0b3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d0b3-115">CommonParameters</span></span>
<span data-ttu-id="1d0b3-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1d0b3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d0b3-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d0b3-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d0b3-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1d0b3-118">INPUTS</span></span>

### <span data-ttu-id="1d0b3-119">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="1d0b3-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="1d0b3-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1d0b3-120">OUTPUTS</span></span>

### <span data-ttu-id="1d0b3-121">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementtenantconfigurationsyncstate</span><span class="sxs-lookup"><span data-stu-id="1d0b3-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span></span>

## <span data-ttu-id="1d0b3-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1d0b3-122">NOTES</span></span>

## <span data-ttu-id="1d0b3-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1d0b3-123">RELATED LINKS</span></span>
