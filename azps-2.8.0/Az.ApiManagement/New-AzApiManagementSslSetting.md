---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: 7c4fb7c2147d7daf3307c2895893198ebe805ff0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753501"
---
# <span data-ttu-id="39b3c-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="39b3c-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="39b3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39b3c-102">SYNOPSIS</span></span>
<span data-ttu-id="39b3c-103">PsApiManagementSslSetting örneği oluşturur</span><span class="sxs-lookup"><span data-stu-id="39b3c-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="39b3c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="39b3c-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39b3c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="39b3c-105">DESCRIPTION</span></span>
<span data-ttu-id="39b3c-106">Bir PsApiManagementSslSetting örneği oluşturmak için yardımcı komutu.</span><span class="sxs-lookup"><span data-stu-id="39b3c-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="39b3c-107">Bu komut New-AzApiManagement komutuyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="39b3c-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="39b3c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="39b3c-108">EXAMPLES</span></span>

### <span data-ttu-id="39b3c-109">Örnek 1: TLS 1,0 hem arka uç hem de ön uçta etkinleştirmek için SSL ayarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="39b3c-109">Example 1 : Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="39b3c-110">Psapsananagementssl1,0 Setting 'in hem ön uç (istemci ve APıM arasında) hem de arka uç (APıM ve arka uç arasında) ile Apsananaağ geçidi</span><span class="sxs-lookup"><span data-stu-id="39b3c-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="39b3c-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="39b3c-111">PARAMETERS</span></span>

### <span data-ttu-id="39b3c-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="39b3c-112">-BackendProtocol</span></span>
<span data-ttu-id="39b3c-113">Arka uç güvenlik protokolü ayarları.</span><span class="sxs-lookup"><span data-stu-id="39b3c-113">Backend Security protocol settings.</span></span> <span data-ttu-id="39b3c-114">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="39b3c-114">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39b3c-115">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="39b3c-115">-CipherSuite</span></span>
<span data-ttu-id="39b3c-116">Belirtilen düzende SSL şifre paketleri ayarları.</span><span class="sxs-lookup"><span data-stu-id="39b3c-116">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="39b3c-117">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="39b3c-117">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39b3c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39b3c-118">-DefaultProfile</span></span>
<span data-ttu-id="39b3c-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="39b3c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39b3c-120">-Frontenvseçprotocol</span><span class="sxs-lookup"><span data-stu-id="39b3c-120">-FrontendProtocol</span></span>
<span data-ttu-id="39b3c-121">Ön uç güvenlik iletişim kuralları ayarları.</span><span class="sxs-lookup"><span data-stu-id="39b3c-121">Frontend Security protocols settings.</span></span> <span data-ttu-id="39b3c-122">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="39b3c-122">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39b3c-123">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="39b3c-123">-ServerProtocol</span></span>
<span data-ttu-id="39b3c-124">Http2 gibi sunucu protokolü ayarları.</span><span class="sxs-lookup"><span data-stu-id="39b3c-124">Server protocol settings like Http2.</span></span> <span data-ttu-id="39b3c-125">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="39b3c-125">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39b3c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39b3c-126">CommonParameters</span></span>
<span data-ttu-id="39b3c-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="39b3c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39b3c-128">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="39b3c-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39b3c-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="39b3c-129">INPUTS</span></span>

### <span data-ttu-id="39b3c-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="39b3c-130">None</span></span>

## <span data-ttu-id="39b3c-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="39b3c-131">OUTPUTS</span></span>

### <span data-ttu-id="39b3c-132">Microsoft. Azure. Commands. apsananad</span><span class="sxs-lookup"><span data-stu-id="39b3c-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="39b3c-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="39b3c-133">NOTES</span></span>

## <span data-ttu-id="39b3c-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="39b3c-134">RELATED LINKS</span></span>

[<span data-ttu-id="39b3c-135">Yeni-azlı bir</span><span class="sxs-lookup"><span data-stu-id="39b3c-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

