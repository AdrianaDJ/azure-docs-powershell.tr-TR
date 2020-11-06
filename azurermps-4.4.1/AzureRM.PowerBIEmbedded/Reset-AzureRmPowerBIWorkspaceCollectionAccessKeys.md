---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
ms.openlocfilehash: 766682df23beaa7c513ff54554a3ebd59a6d1537
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594209"
---
# <span data-ttu-id="baad4-101">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="baad4-101">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>

## <span data-ttu-id="baad4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baad4-102">SYNOPSIS</span></span>
<span data-ttu-id="baad4-103">Belirtilen Access tuşunu sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="baad4-103">Resets the specified access key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="baad4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="baad4-104">SYNTAX</span></span>

```
Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys [-ResourceGroupName] <String>
 [-WorkspaceCollectionName] <String> [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="baad4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="baad4-105">DESCRIPTION</span></span>
<span data-ttu-id="baad4-106">**Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet 'ı Power BI çalışma alanı koleksiyonunuzda belirtilen Access tuşunu sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="baad4-106">The **Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="baad4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="baad4-107">EXAMPLES</span></span>

### <span data-ttu-id="baad4-108">Örnek 1: birincil erişim anahtarını sıfırlama</span><span class="sxs-lookup"><span data-stu-id="baad4-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="baad4-109">Bu komut, belirtilen kaynak grubundaki WCN11 adındaki çalışma alanı koleksiyonu için birincil erişim anahtarını sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="baad4-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="baad4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="baad4-110">PARAMETERS</span></span>

### <span data-ttu-id="baad4-111">-Anahtar</span><span class="sxs-lookup"><span data-stu-id="baad4-111">-Key1</span></span>
<span data-ttu-id="baad4-112">Bu cmdlet 'in birincil erişim anahtarını sıfırtığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="baad4-112">Indicates that this cmdlet resets the primary access key.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baad4-113">-Anahtar2</span><span class="sxs-lookup"><span data-stu-id="baad4-113">-Key2</span></span>
<span data-ttu-id="baad4-114">Bu cmdlet 'in ikincil erişim tuşunu sıfırtığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="baad4-114">Indicates that this cmdlet resets the secondary access key.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baad4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baad4-115">-ResourceGroupName</span></span>
<span data-ttu-id="baad4-116">Koleksiyonun kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="baad4-116">Specifies the name of the resource group of the collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baad4-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="baad4-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="baad4-118">Bu cmdlet 'in üzerinde çalıştırıldığı Power BI çalışma alanı koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="baad4-118">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baad4-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="baad4-119">-Confirm</span></span>
<span data-ttu-id="baad4-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="baad4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="baad4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baad4-121">-WhatIf</span></span>
<span data-ttu-id="baad4-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="baad4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="baad4-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="baad4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="baad4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baad4-124">-DefaultProfile</span></span>
<span data-ttu-id="baad4-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="baad4-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="baad4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baad4-126">CommonParameters</span></span>
<span data-ttu-id="baad4-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="baad4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baad4-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baad4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baad4-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="baad4-129">INPUTS</span></span>

## <span data-ttu-id="baad4-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="baad4-130">OUTPUTS</span></span>

### <span data-ttu-id="baad4-131">Microsoft. Azure. Commands. Management. PowerBIEmbedded. model. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="baad4-131">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="baad4-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="baad4-132">NOTES</span></span>

## <span data-ttu-id="baad4-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="baad4-133">RELATED LINKS</span></span>

[<span data-ttu-id="baad4-134">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="baad4-134">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>](./Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md)


