---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsamplingsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSamplingSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSamplingSetting.md
ms.openlocfilehash: 12f0aa4d198a93d1e392aa61294de6e5815196b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753503"
---
# <span data-ttu-id="7e770-101">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="7e770-101">New-AzApiManagementSamplingSetting</span></span>

## <span data-ttu-id="7e770-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e770-102">SYNOPSIS</span></span>
<span data-ttu-id="7e770-103">Tanılama için yeni bir örnekleme ayarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="7e770-103">Create a new sampling setting for the Diagnostic</span></span>

## <span data-ttu-id="7e770-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7e770-104">SYNTAX</span></span>

```
New-AzApiManagementSamplingSetting [-SamplingType <String>] [-SamplingPercentage <Double>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e770-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7e770-105">DESCRIPTION</span></span>
<span data-ttu-id="7e770-106">**Yeni-Azapsananagementörnekle**</span><span class="sxs-lookup"><span data-stu-id="7e770-106">The cmdlet **New-AzApiManagementSamplingSetting** creates a new sampling setting for the Diagnostic</span></span>

## <span data-ttu-id="7e770-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7e770-107">EXAMPLES</span></span>

### <span data-ttu-id="7e770-108">Örnek 1: temel bir örnekleme ayarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="7e770-108">Example 1 : Create a basic Sampling setting</span></span>
```powershell
PS C:\> New-AzApiManagementSamplingSetting -SamplingType fixed -Percentage 100

SamplingType Percentage
------------ ----------
fixed               100
```

<span data-ttu-id="7e770-109">`Fixed`İsteklerin/yanıtların %100 için günlüğe kaydetme ile türde bir örnekleme ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="7e770-109">Creates a sampling setting of `Fixed` type with logging for 100% of the requests / responses</span></span>

## <span data-ttu-id="7e770-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7e770-110">PARAMETERS</span></span>

### <span data-ttu-id="7e770-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e770-111">-DefaultProfile</span></span>
<span data-ttu-id="7e770-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7e770-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e770-113">-SamplingPercentage</span><span class="sxs-lookup"><span data-stu-id="7e770-113">-SamplingPercentage</span></span>
<span data-ttu-id="7e770-114">Sabit oran örnekleme için örnekleme oranı.</span><span class="sxs-lookup"><span data-stu-id="7e770-114">Rate of Sampling for Fixed Rate Sampling.</span></span> <span data-ttu-id="7e770-115">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="7e770-115">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e770-116">-SamplingType</span><span class="sxs-lookup"><span data-stu-id="7e770-116">-SamplingType</span></span>
<span data-ttu-id="7e770-117">Örnekleme türü.</span><span class="sxs-lookup"><span data-stu-id="7e770-117">The Type of Sampling.</span></span>
<span data-ttu-id="7e770-118">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="7e770-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e770-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e770-119">CommonParameters</span></span>
<span data-ttu-id="7e770-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7e770-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e770-121">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7e770-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e770-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7e770-122">INPUTS</span></span>

### <span data-ttu-id="7e770-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7e770-123">None</span></span>

## <span data-ttu-id="7e770-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7e770-124">OUTPUTS</span></span>

### <span data-ttu-id="7e770-125">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementsampsetting</span><span class="sxs-lookup"><span data-stu-id="7e770-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

## <span data-ttu-id="7e770-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7e770-126">NOTES</span></span>

## <span data-ttu-id="7e770-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7e770-127">RELATED LINKS</span></span>

[<span data-ttu-id="7e770-128">Get-Azapsananagementdiagnostic</span><span class="sxs-lookup"><span data-stu-id="7e770-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="7e770-129">Remove-Azapsananagementdiagnostic</span><span class="sxs-lookup"><span data-stu-id="7e770-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="7e770-130">Set-Azapsananagementdiagnostic</span><span class="sxs-lookup"><span data-stu-id="7e770-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="7e770-131">Yeni-Azapsanana,</span><span class="sxs-lookup"><span data-stu-id="7e770-131">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)
