---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3302054E-C5BB-4B89-B9C9-ED7572DFA234
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: 7c7afc0a1b6544f165f379a7363960142f73780d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763960"
---
# <span data-ttu-id="6ea12-101">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="6ea12-101">Remove-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="6ea12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ea12-102">SYNOPSIS</span></span>
<span data-ttu-id="6ea12-103">Geçerli kasadan site kurtarma sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6ea12-103">Removes a Site Recovery server from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ea12-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ea12-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServer -Server <ASRServer> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ea12-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ea12-105">DESCRIPTION</span></span>
<span data-ttu-id="6ea12-106">**Remove-AzureRmSiteRecoveryServer** cmdlet 'i geçerli kasadan kaldıran bir Azure Site kurtarma sunucusu kaydını siler.</span><span class="sxs-lookup"><span data-stu-id="6ea12-106">The **Remove-AzureRmSiteRecoveryServer** cmdlet unregisters an Azure Site Recovery server which removes it from the current vault.</span></span>

## <span data-ttu-id="6ea12-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ea12-107">EXAMPLES</span></span>

## <span data-ttu-id="6ea12-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ea12-108">PARAMETERS</span></span>

### <span data-ttu-id="6ea12-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ea12-109">-DefaultProfile</span></span>
<span data-ttu-id="6ea12-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6ea12-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ea12-111">-Force</span><span class="sxs-lookup"><span data-stu-id="6ea12-111">-Force</span></span>
<span data-ttu-id="6ea12-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="6ea12-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ea12-113">-Sunucu</span><span class="sxs-lookup"><span data-stu-id="6ea12-113">-Server</span></span>
<span data-ttu-id="6ea12-114">Site kurtarma sunucusu nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ea12-114">Specifies the Site Recovery server object.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ea12-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="6ea12-115">-Confirm</span></span>
<span data-ttu-id="6ea12-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6ea12-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ea12-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ea12-117">-WhatIf</span></span>
<span data-ttu-id="6ea12-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6ea12-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="6ea12-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6ea12-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ea12-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ea12-120">CommonParameters</span></span>
<span data-ttu-id="6ea12-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ea12-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ea12-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ea12-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ea12-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ea12-123">INPUTS</span></span>

### <span data-ttu-id="6ea12-124">ASRServer</span><span class="sxs-lookup"><span data-stu-id="6ea12-124">ASRServer</span></span>
<span data-ttu-id="6ea12-125">' Server ' parametresi ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="6ea12-125">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="6ea12-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ea12-126">OUTPUTS</span></span>

### <span data-ttu-id="6ea12-127">System. Koleksiyonlar. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRServer]</span><span class="sxs-lookup"><span data-stu-id="6ea12-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="6ea12-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ea12-128">NOTES</span></span>

## <span data-ttu-id="6ea12-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ea12-129">RELATED LINKS</span></span>

[<span data-ttu-id="6ea12-130">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="6ea12-130">Get-AzureRmSiteRecoveryServer</span></span>](./Get-AzureRmSiteRecoveryServer.md)

[<span data-ttu-id="6ea12-131">Güncelleştirme-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="6ea12-131">Update-AzureRmSiteRecoveryServer</span></span>](./Update-AzureRmSiteRecoveryServer.md)
