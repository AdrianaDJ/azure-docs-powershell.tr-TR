---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/reset-azurermpowerbiworkspacecollectionaccesskeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
ms.openlocfilehash: cb8236acfc0fd1d349091593a2510da271820020
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764603"
---
# <span data-ttu-id="c102e-101">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="c102e-101">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>

## <span data-ttu-id="c102e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c102e-102">SYNOPSIS</span></span>
<span data-ttu-id="c102e-103">Belirtilen Access tuşunu sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="c102e-103">Resets the specified access key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c102e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c102e-104">SYNTAX</span></span>

```
Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys [-ResourceGroupName] <String>
 [-WorkspaceCollectionName] <String> [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c102e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c102e-105">DESCRIPTION</span></span>
<span data-ttu-id="c102e-106">**Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet 'ı Power BI çalışma alanı koleksiyonunuzda belirtilen Access tuşunu sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="c102e-106">The **Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="c102e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c102e-107">EXAMPLES</span></span>

### <span data-ttu-id="c102e-108">Örnek 1: birincil erişim anahtarını sıfırlama</span><span class="sxs-lookup"><span data-stu-id="c102e-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="c102e-109">Bu komut, belirtilen kaynak grubundaki WCN11 adındaki çalışma alanı koleksiyonu için birincil erişim anahtarını sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="c102e-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="c102e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c102e-110">PARAMETERS</span></span>

### <span data-ttu-id="c102e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c102e-111">-DefaultProfile</span></span>
<span data-ttu-id="c102e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c102e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c102e-113">-Anahtar</span><span class="sxs-lookup"><span data-stu-id="c102e-113">-Key1</span></span>
<span data-ttu-id="c102e-114">Bu cmdlet 'in birincil erişim anahtarını sıfırtığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c102e-114">Indicates that this cmdlet resets the primary access key.</span></span>

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

### <span data-ttu-id="c102e-115">-Anahtar2</span><span class="sxs-lookup"><span data-stu-id="c102e-115">-Key2</span></span>
<span data-ttu-id="c102e-116">Bu cmdlet 'in ikincil erişim tuşunu sıfırtığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c102e-116">Indicates that this cmdlet resets the secondary access key.</span></span>

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

### <span data-ttu-id="c102e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c102e-117">-ResourceGroupName</span></span>
<span data-ttu-id="c102e-118">Koleksiyonun kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c102e-118">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="c102e-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="c102e-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="c102e-120">Bu cmdlet 'in üzerinde çalıştırıldığı Power BI çalışma alanı koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c102e-120">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c102e-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="c102e-121">-Confirm</span></span>
<span data-ttu-id="c102e-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c102e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c102e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c102e-123">-WhatIf</span></span>
<span data-ttu-id="c102e-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c102e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c102e-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c102e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c102e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c102e-126">CommonParameters</span></span>
<span data-ttu-id="c102e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c102e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c102e-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c102e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c102e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c102e-129">INPUTS</span></span>

### <span data-ttu-id="c102e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c102e-130">System.String</span></span>

## <span data-ttu-id="c102e-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c102e-131">OUTPUTS</span></span>

### <span data-ttu-id="c102e-132">Microsoft. Azure. Commands. Management. PowerBIEmbedded. model. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="c102e-132">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="c102e-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c102e-133">NOTES</span></span>

## <span data-ttu-id="c102e-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c102e-134">RELATED LINKS</span></span>

[<span data-ttu-id="c102e-135">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="c102e-135">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>](./Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md)


