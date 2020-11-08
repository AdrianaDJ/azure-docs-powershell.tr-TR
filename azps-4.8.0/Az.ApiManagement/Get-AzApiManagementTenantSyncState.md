---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
ms.openlocfilehash: 233c74e3939884cd4bd311ec463d81d7e7613f31
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109253"
---
# <span data-ttu-id="60039-101">Get-AzApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="60039-101">Get-AzApiManagementTenantSyncState</span></span>

## <span data-ttu-id="60039-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60039-102">SYNOPSIS</span></span>
<span data-ttu-id="60039-103">Yapılandırma veritabanıyla git deposu arasındaki en son eşitlemenin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="60039-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="60039-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="60039-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantSyncState -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="60039-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="60039-105">DESCRIPTION</span></span>
<span data-ttu-id="60039-106">**Get-Azapsananagementtenantsyncstate** cmdlet 'i, yapılandırma veritabanı ile git deposu arasındaki en son eşitlemenin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="60039-106">The **Get-AzApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="60039-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="60039-107">EXAMPLES</span></span>

### <span data-ttu-id="60039-108">Örnek 1: en son eşitlemenin durumunu alma</span><span class="sxs-lookup"><span data-stu-id="60039-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantSyncState -Context $apimContext
```

<span data-ttu-id="60039-109">Bu komut, yapılandırma veritabanıyla git deposu arasındaki en son eşitlemenin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="60039-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="60039-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="60039-110">PARAMETERS</span></span>

### <span data-ttu-id="60039-111">-Context</span><span class="sxs-lookup"><span data-stu-id="60039-111">-Context</span></span>
<span data-ttu-id="60039-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="60039-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="60039-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60039-113">-DefaultProfile</span></span>
<span data-ttu-id="60039-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="60039-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60039-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60039-115">CommonParameters</span></span>
<span data-ttu-id="60039-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="60039-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60039-117">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="60039-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60039-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="60039-118">INPUTS</span></span>

### <span data-ttu-id="60039-119">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="60039-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="60039-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="60039-120">OUTPUTS</span></span>

### <span data-ttu-id="60039-121">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementtenantconfigurationsyncstate</span><span class="sxs-lookup"><span data-stu-id="60039-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span></span>

## <span data-ttu-id="60039-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="60039-122">NOTES</span></span>

## <span data-ttu-id="60039-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="60039-123">RELATED LINKS</span></span>
