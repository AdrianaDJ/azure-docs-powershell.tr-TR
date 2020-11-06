---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 16a48b6f945aac8ef287ff612d64da1273add521
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587033"
---
# <span data-ttu-id="422ab-101">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="422ab-101">Remove-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="422ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="422ab-102">SYNOPSIS</span></span>
<span data-ttu-id="422ab-103">Yetkilendirme sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="422ab-103">Removes an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="422ab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="422ab-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="422ab-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="422ab-105">DESCRIPTION</span></span>
<span data-ttu-id="422ab-106">**Remove-Azurermapsananagementauthorizationserver** cmdlet 'ı BIR Azure API yönetim yetkilendirme sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="422ab-106">The **Remove-AzureRmApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="422ab-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="422ab-107">EXAMPLES</span></span>

## <span data-ttu-id="422ab-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="422ab-108">PARAMETERS</span></span>

### <span data-ttu-id="422ab-109">-Context</span><span class="sxs-lookup"><span data-stu-id="422ab-109">-Context</span></span>
<span data-ttu-id="422ab-110">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="422ab-110">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="422ab-111">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="422ab-111">-PassThru</span></span>
<span data-ttu-id="422ab-112">geçiş</span><span class="sxs-lookup"><span data-stu-id="422ab-112">passthru</span></span>

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

### <span data-ttu-id="422ab-113">-SunucuKimliği</span><span class="sxs-lookup"><span data-stu-id="422ab-113">-ServerId</span></span>
<span data-ttu-id="422ab-114">Kaldırılacak yetkilendirme sunucusunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="422ab-114">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="422ab-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="422ab-115">-Confirm</span></span>
<span data-ttu-id="422ab-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="422ab-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="422ab-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="422ab-117">-WhatIf</span></span>
<span data-ttu-id="422ab-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="422ab-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="422ab-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="422ab-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="422ab-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="422ab-120">-DefaultProfile</span></span>
<span data-ttu-id="422ab-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="422ab-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="422ab-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="422ab-122">CommonParameters</span></span>
<span data-ttu-id="422ab-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="422ab-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="422ab-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="422ab-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="422ab-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="422ab-125">INPUTS</span></span>

## <span data-ttu-id="422ab-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="422ab-126">OUTPUTS</span></span>

### <span data-ttu-id="422ab-127">Boole</span><span class="sxs-lookup"><span data-stu-id="422ab-127">Boolean</span></span>

## <span data-ttu-id="422ab-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="422ab-128">NOTES</span></span>

## <span data-ttu-id="422ab-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="422ab-129">RELATED LINKS</span></span>

[<span data-ttu-id="422ab-130">Get-Azurermapımanagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="422ab-130">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="422ab-131">Yeni-Azurermapımanagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="422ab-131">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="422ab-132">Set-Azurermapımanagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="422ab-132">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


