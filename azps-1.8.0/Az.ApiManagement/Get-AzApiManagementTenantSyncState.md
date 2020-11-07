---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
ms.openlocfilehash: a883da9c32c909801f9b7c1a795bd513ada737d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751140"
---
# <span data-ttu-id="c8215-101">Get-AzApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="c8215-101">Get-AzApiManagementTenantSyncState</span></span>

## <span data-ttu-id="c8215-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8215-102">SYNOPSIS</span></span>
<span data-ttu-id="c8215-103">Yapılandırma veritabanıyla git deposu arasındaki en son eşitlemenin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="c8215-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="c8215-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c8215-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantSyncState -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8215-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c8215-105">DESCRIPTION</span></span>
<span data-ttu-id="c8215-106">**Get-Azapsananagementtenantsyncstate** cmdlet 'i, yapılandırma veritabanı ile git deposu arasındaki en son eşitlemenin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="c8215-106">The **Get-AzApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="c8215-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c8215-107">EXAMPLES</span></span>

### <span data-ttu-id="c8215-108">Örnek 1: en son eşitlemenin durumunu alma</span><span class="sxs-lookup"><span data-stu-id="c8215-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantSyncState -Context $apimContext
```

<span data-ttu-id="c8215-109">Bu komut, yapılandırma veritabanıyla git deposu arasındaki en son eşitlemenin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="c8215-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="c8215-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c8215-110">PARAMETERS</span></span>

### <span data-ttu-id="c8215-111">-Context</span><span class="sxs-lookup"><span data-stu-id="c8215-111">-Context</span></span>
<span data-ttu-id="c8215-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8215-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c8215-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8215-113">-DefaultProfile</span></span>
<span data-ttu-id="c8215-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c8215-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8215-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8215-115">CommonParameters</span></span>
<span data-ttu-id="c8215-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c8215-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8215-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8215-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8215-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c8215-118">INPUTS</span></span>

### <span data-ttu-id="c8215-119">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="c8215-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="c8215-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c8215-120">OUTPUTS</span></span>

### <span data-ttu-id="c8215-121">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementtenantconfigurationsyncstate</span><span class="sxs-lookup"><span data-stu-id="c8215-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span></span>

## <span data-ttu-id="c8215-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c8215-122">NOTES</span></span>

## <span data-ttu-id="c8215-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c8215-123">RELATED LINKS</span></span>
