---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: 709e8483a5f21e3afc58add1046b5dae22bea7b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097687"
---
# <span data-ttu-id="e97d1-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="e97d1-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="e97d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e97d1-102">SYNOPSIS</span></span>
<span data-ttu-id="e97d1-103">PsApiManagementSslSetting örneği oluşturur</span><span class="sxs-lookup"><span data-stu-id="e97d1-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="e97d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e97d1-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e97d1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e97d1-105">DESCRIPTION</span></span>
<span data-ttu-id="e97d1-106">Bir PsApiManagementSslSetting örneği oluşturmak için yardımcı komutu.</span><span class="sxs-lookup"><span data-stu-id="e97d1-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="e97d1-107">Bu komut New-AzApiManagement komutuyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e97d1-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="e97d1-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e97d1-108">EXAMPLES</span></span>

### <span data-ttu-id="e97d1-109">Örnek 1: TLS 1,0 hem arka uç hem de ön uçta etkinleştirmek için SSL ayarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="e97d1-109">Example 1 : Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="e97d1-110">Psapsananagementssl1,0 Setting 'in hem ön uç (istemci ve APıM arasında) hem de arka uç (APıM ve arka uç arasında) ile Apsananaağ geçidi</span><span class="sxs-lookup"><span data-stu-id="e97d1-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="e97d1-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e97d1-111">PARAMETERS</span></span>

### <span data-ttu-id="e97d1-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="e97d1-112">-BackendProtocol</span></span>
<span data-ttu-id="e97d1-113">Arka uç güvenlik protokolü ayarları.</span><span class="sxs-lookup"><span data-stu-id="e97d1-113">Backend Security protocol settings.</span></span> <span data-ttu-id="e97d1-114">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e97d1-114">This parameter is optional.</span></span>
<span data-ttu-id="e97d1-115">Geçerli protokol ayarları: `Tls11` -tls 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0</span><span class="sxs-lookup"><span data-stu-id="e97d1-115">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>

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

### <span data-ttu-id="e97d1-116">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="e97d1-116">-CipherSuite</span></span>
<span data-ttu-id="e97d1-117">Belirtilen düzende SSL şifre paketleri ayarları.</span><span class="sxs-lookup"><span data-stu-id="e97d1-117">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="e97d1-118">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e97d1-118">This parameter is optional.</span></span>
<span data-ttu-id="e97d1-119">Geçerli ayarlar şunlardır: `TripleDes168` üç durumlu PE Des 168</span><span class="sxs-lookup"><span data-stu-id="e97d1-119">The valid Settings are `TripleDes168` - Enable / Disable Tripe Des 168</span></span>

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

### <span data-ttu-id="e97d1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e97d1-120">-DefaultProfile</span></span>
<span data-ttu-id="e97d1-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e97d1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e97d1-122">-Frontenvseçprotocol</span><span class="sxs-lookup"><span data-stu-id="e97d1-122">-FrontendProtocol</span></span>
<span data-ttu-id="e97d1-123">Ön uç güvenlik iletişim kuralları ayarları.</span><span class="sxs-lookup"><span data-stu-id="e97d1-123">Frontend Security protocols settings.</span></span> <span data-ttu-id="e97d1-124">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e97d1-124">This parameter is optional.</span></span>
<span data-ttu-id="e97d1-125">Geçerli protokol ayarları: `Tls11` -tls 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0</span><span class="sxs-lookup"><span data-stu-id="e97d1-125">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>


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

### <span data-ttu-id="e97d1-126">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="e97d1-126">-ServerProtocol</span></span>
<span data-ttu-id="e97d1-127">Http2 gibi sunucu protokolü ayarları.</span><span class="sxs-lookup"><span data-stu-id="e97d1-127">Server protocol settings like Http2.</span></span> <span data-ttu-id="e97d1-128">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e97d1-128">This parameter is optional.</span></span>
<span data-ttu-id="e97d1-129">Geçerli ayarlar şunlardır: `Http2` Http 2,0</span><span class="sxs-lookup"><span data-stu-id="e97d1-129">The valid Settings are `Http2` - Enable Http 2.0</span></span>

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

### <span data-ttu-id="e97d1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e97d1-130">CommonParameters</span></span>
<span data-ttu-id="e97d1-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e97d1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e97d1-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e97d1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e97d1-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e97d1-133">INPUTS</span></span>

### <span data-ttu-id="e97d1-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e97d1-134">None</span></span>

## <span data-ttu-id="e97d1-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e97d1-135">OUTPUTS</span></span>

### <span data-ttu-id="e97d1-136">Microsoft. Azure. Commands. apsananad</span><span class="sxs-lookup"><span data-stu-id="e97d1-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="e97d1-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e97d1-137">NOTES</span></span>

## <span data-ttu-id="e97d1-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e97d1-138">RELATED LINKS</span></span>

[<span data-ttu-id="e97d1-139">Yeni-azlı bir</span><span class="sxs-lookup"><span data-stu-id="e97d1-139">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

