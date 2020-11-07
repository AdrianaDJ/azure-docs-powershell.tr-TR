---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: b9b6092035d97aed8f70137c4157bfb80bf3f62a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759811"
---
# <span data-ttu-id="6c31d-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="6c31d-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="6c31d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c31d-102">SYNOPSIS</span></span>
<span data-ttu-id="6c31d-103">Power BI çalışma alanı koleksiyonuyla ilişkili geçerli erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="6c31d-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="6c31d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6c31d-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c31d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6c31d-105">DESCRIPTION</span></span>
<span data-ttu-id="6c31d-106">**Get-AzPowerBIWorkspaceCollectionAccessKey** cmdlet 'ı, Power BI çalışma alanı koleksiyonuyla ilişkili geçerli erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="6c31d-106">The **Get-AzPowerBIWorkspaceCollectionAccessKey** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="6c31d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6c31d-107">EXAMPLES</span></span>

### <span data-ttu-id="6c31d-108">Örnek 1: erişim tuşlarını alın</span><span class="sxs-lookup"><span data-stu-id="6c31d-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="6c31d-109">Bu komut, belirtilen kaynak grubundaki WCN11 adındaki çalışma alanı koleksiyonu için erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="6c31d-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="6c31d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6c31d-110">PARAMETERS</span></span>

### <span data-ttu-id="6c31d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c31d-111">-DefaultProfile</span></span>
<span data-ttu-id="6c31d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6c31d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c31d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c31d-113">-ResourceGroupName</span></span>
<span data-ttu-id="6c31d-114">Koleksiyonun kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c31d-114">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="6c31d-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="6c31d-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="6c31d-116">Bu cmdlet 'in üzerinde çalıştırıldığı Power BI çalışma alanı koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c31d-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="6c31d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c31d-117">CommonParameters</span></span>
<span data-ttu-id="6c31d-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6c31d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c31d-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c31d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c31d-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6c31d-120">INPUTS</span></span>

### <span data-ttu-id="6c31d-121">System. String</span><span class="sxs-lookup"><span data-stu-id="6c31d-121">System.String</span></span>

## <span data-ttu-id="6c31d-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6c31d-122">OUTPUTS</span></span>

### <span data-ttu-id="6c31d-123">Microsoft. Azure. Commands. Management. PowerBIEmbedded. model. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="6c31d-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="6c31d-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6c31d-124">NOTES</span></span>

## <span data-ttu-id="6c31d-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6c31d-125">RELATED LINKS</span></span>

[<span data-ttu-id="6c31d-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="6c31d-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Reset-AzPowerBIWorkspaceCollectionAccessKey.md)


